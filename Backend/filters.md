# Filters & Sorting
Following is the explanation on how filters and sorting on members is implemented. 

### Filters

###### Basic usage
Query string based filtering & sorting operations is allowed. It can by used by `Spatie\QueryBuilder\QueryBuilder` facade.

Filter a query based on a request: `/members?filter[full_name]=Mehul`
```
QueryBuilder::for(Member::class)
    ->allowedFilters('full_name')
    ->get();
```
###### Filtering
The filter query parameters can be used to add where clauses to your Eloquent query.
By default, all filters have to be explicitly allowed using `allowedFilters()`. This method takes an array of strings or AllowedFilter instances. An allowed filter can be partial, exact, scope or custom. By default, any string values passed to `allowedFilters()` will automatically be converted to `AllowedFilter::partial()` filters.

###### Scope filters
Sometimes more advanced filtering options are necessary. This is where scope filters, callback filters and custom filters come in handy.
Scope filters allows us to add local scopes to our query by adding filters to the URL.

On `Models/Member.php` model there are multiple scopes defined which we're making use of in `API/MembersController.php`.

For example:

```
public function scopePhone($query, $phone)
{
    return $query->where('mobile_number', 'LIKE', "%{$phone}%")
        ->orWhere('whatsapp_number', 'LIKE', "%{$phone}%");
}
```

```
AllowedFilter::scope('phone'),
```
```
GET /members?filter[phone]=9979912312
```
Above request will only return members who has a phone number like `9979912312`

### Sorting
The `sort` query parameter is used to determine by which property the results collection will be ordered. Sorting is ascending by default and can be reversed by adding a hyphen (-) to the start of 
the property name.

All sorts have to be explicitly allowed by passing an array to the`allowedSorts()` method. The allowedSorts method takes an array of column names as strings or instances of AllowedSorts.

###### Basic usage

```
 GET /members?sort=-first_name
```

```
allowedSorts(['id','first_name'])
```
Above example will return dataset sorted by `first_name` in descending order. If you want the opposite result, You may do so like this:
```
GET /members?sort=+first_name
```