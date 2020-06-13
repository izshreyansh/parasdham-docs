# Authentication
Our backend uses API Token based authentication. Therefore on the frontend we provide Vuex based state managed Authentication.

The application grantflow is as follows: 
1. User enters credentials
2. Frontend makes call to authentication service, User is granted an API Token.
3. We'll save this token in Vuex state store.
4. We'll attach this api token with each call to the backend otherwise backend will reply with http 401 status code. (Refer to `src\main.js`)

> By default Vuex states are non persistent. Which means if the user navigates away then the State information will be instantly lost. To mitigate this issue we use `vuex-persistedstate` vue plugin. Which stores the vuex in local storage in the browser.

###### Token Invalidate & Logout
On the frontend side, We rely on the server to invalidate tokens. Therefore by using `AXIOS` interceptor, We'll reset the vuex store whenever backend replies with status code `401 unauthenticated`. This configuration can be modified at `src\App.vue`. Basically deleting a vuex store session is equivalent to clearing a session in a MPA application.

Authentication store can be found at `src\state\store.js`. This store handles authentication for `Member` as well as `User` (Maintainers).

### Authorisation
On the `src\state\store.js` vuex store, `user` getter function will give us `User` object. This is stored at the time of user login, along with: `permissions` for the logged-in user. Permissions can be retrieved by `permissions` getter.

We use `permission` getter to interlink User Gates Policy at `src\gates.js`. Once gates are defined for a given permission. We're ready to authorise users for that permission.

In-order to use this policy you can use this snippet.
```
<li v-if="$can('crud', 'members')">
    <router-link tag="a" :to="{name: 'Member Create' }" class="side-nav-link-ref">
        Create
    </router-link>
</li>
```
> :warning: Here `crud` is function on MembersPolicy at `src\gates.js`