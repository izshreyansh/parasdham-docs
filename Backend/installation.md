# Installation
This guide assumes that you're familiar with setting up [Laravel application](https://laravel.com/docs/7.x/).

## Setting up the project
First step is cloning the project in the repository of your choice. Next is as follow.

1. copy .env.example to .env
2. Run `composer install`
3. Run `php artisan key:generate`
4. Copy `.env.example` to `.env`
Update your desired setings. 
5. It is important to set `database`,`mail`,`cache` driver in your `.env` according to your environment.
	
> If you use `redis`,  All the settings have already been configured. However if you go with memcached,dynamodb etc. You'll have to figure out its dependencies.

6. In your `.env` file, Also add `twillio` & `hakimi`auth details.

7. Run `php artisan migrate` 
   (Optionally add `--seed` if you don't have database-dump.sql)

8. Set `SCOUT_DRIVER` to [tntsearch](https://github.com/teamtnt/laravel-scout-tntsearch-driver#installation)
   
   > In `config/scout.php` you will find array called `tntsearch` it is responsible for creating indexes for search in our application. You want to make sure that user www-data has proper write permission to storage_path.
