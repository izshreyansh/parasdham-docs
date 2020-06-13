# Installation
Setting up the front-end is as straight forward as installing dependencies & building static files.
Let's checkout how we can go about that.

### Deploy locally

1. Clone the frontend repository.
2. Make sure you have following installed locally on your local machine / web server.
    - [Node JS](https://nodejs.org/en/download/)
	- [npm](https://www.npmjs.com/get-npm)
	- [Vue cli](https://cli.vuejs.org/guide/installation.html) `Only required if running locally`
3. Install all npm dependencies by running: `npm install`.
4. Set backend api url in `.env` file.
5. Assuming you're running this on your local machine & you have vue-cli installed. You can run `npm run serve` in-order to start an npm server.

> :bulb: For Production: Remember to set environment variable keyed by `VUE_APP_API_URL` equal to the backend api url.

### Deploy on Netlify
1. Create new site & allow access to the front-end repository.
2. In the build/deploy settings enter following settings:

| Config | Value     |
| ---- | ---- |
|Base directory |      |
|Build command | npm run build |
|Publish Directory | /dist |
|Builds | Active Builds |

### GitHub Pages

1. Set correct `publicPath` in `vue.config.js`.

    If you are deploying to `https://<USERNAME>.github.io/`, you can omit `publicPath` as it defaults to `"/"`.

    If you are deploying to `https://<USERNAME>.github.io/<REPO>/`, (i.e. your repository is at `https://github.com/<USERNAME>/<REPO>`), set `publicPath` to `"/<REPO>/"`. For example, if your repo name is "my-project", your `vue.config.js` should look like this:

    ```
    js
    module.exports = {
      publicPath: process.env.NODE_ENV === 'production'
        ? '/my-project/'
        : '/'
    }
    ```

2. Inside your project, create `deploy.sh` with the following content (with highlighted lines uncommented appropriately) and run it to deploy:

    ```
    bash{13,20,23}
    #!/usr/bin/env sh

    # abort on errors
    set -e

    # build
    npm run build

    # navigate into the build output directory
    cd dist

    # if you are deploying to a custom domain
    # echo 'www.example.com' > CNAME

    git init
    git add -A
    git commit -m 'deploy'

    # if you are deploying to https://<USERNAME>.github.io
    # git push -f git@github.com:<USERNAME>/<USERNAME>.github.io.git master

    # if you are deploying to https://<USERNAME>.github.io/<REPO>
    # git push -f git@github.com:<USERNAME>/<REPO>.git master:gh-pages

    cd -
    ```

### GitLab Pages

As described by [GitLab Pages documentation](https://docs.gitlab.com/ee/user/project/pages/), everything happens with a `.gitlab-ci.yml` file placed in the root of your repository. This working example will get you started:

```
# .gitlab-ci.yml file to be placed in the root of your repository

pages: # the job must be named pages
  image: node:latest
  stage: deploy
  script:
    - npm ci
    - npm run build
    - mv public public-vue # GitLab Pages hooks on the public folder
    - mv dist public # rename the dist folder (result of npm run build)
    # optionally, you can activate gzip support wih the following line:
    - find public -type f -regex '.*\.\(htm\|html\|txt\|text\|js\|css\)$' -exec gzip -f -k {} \;
  artifacts:
    paths:
      - public # artifact path must be /public for GitLab Pages to pick it up
  only:
    - master
```

> Please read through the docs on [GitLab Pages domains](https://docs.gitlab.com/ee/user/project/pages/getting_started_part_one.html#gitlab-pages-domain) for more info about the URL where your project website will be hosted.