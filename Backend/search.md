# Search
For record searching using fuzzy search, We're using 1st party plugin: [scout](https://laravel.com/docs/7.x/scout#introduction). Laravel Scout provides a simple, driver based solution for adding full-text search to our Eloquent models. Using model observers, Scout will automatically keep our search indexes in sync with Eloquent records.

Laravel comes with algolia driver for search. However it's a paid service & our requirements doesn't match with that service. Therefore we make use of self hosted/managed TNTSearch plugin for Scout. On top of scout's feature, TNT Search gives us few more benefits:
Fuzzy search, Search as you type, Text classification etc.

If you want to fiddle with Global Search fuzziness, You may head over at `\config\scout.php` & scroll down to `tntsearch` array. You'll find we have freedom to change index storage location, Fuzziness etc.

> Scout will keep the index file up to date. However if you've made changes directly to the database. You can rebuild the index with: `php artisan scout:import "App\Models\Member"`. 

> Contrary you can also flush the index using: `php artisan scout:flush "App\Models\Member"` 

Fuzzy search is mainly used at 2 spots. 
1. Global Search
	Global search will hit the `App\Http\Controllers\API\SearchController` & TNTSearch will take it from there to allow for full text search.

2. Member de-duplication logic
	For the ease of use & to keep the concerns coupled. You'll find the de-duplication logic on `Models\Member@getDuplicates` static function. 

You just have to pass the suspected duplicate data set in this format: 

```
	[
    	'first_name' => 'Manish',
		'last_name' => 'Malhotra'
    ]
```
If we have the duplicate in the database, This function will fetch the duplicate from the db & return it. 