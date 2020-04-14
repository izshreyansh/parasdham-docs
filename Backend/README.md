# Introduction
You can find Laravel installation [documentation](https://laravel.com/docs/6.x/) here 

## Setting up the project
First step is cloning the project in the repository of your choice. Next is as follow.

1. copy .env.example to .env
2. Run `composer install`
3. Set your database environment details in .env file.
4. Run `php artisan migrate` 
   (Optionally add `--seed` if you don't have database-dump.sql)

5. Set `SCOUT_DRIVER` to `[tntsearch](https://github.com/teamtnt/laravel-scout-tntsearch-driver#installation)`
   > In `config/scout.php` you will find array called `tntsearch` it is responsible for creating indexes for search in our application. You want to make sure that user www-data has proper write permission to storage_path.
   
