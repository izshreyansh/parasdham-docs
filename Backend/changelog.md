# Automatic Activity Log

All models makes use of [Spatie's Activity Log](https://docs.spatie.be/laravel-activitylog/v3/introduction/) to log every changes to the model.

This functionality is provided by making use of this trait `Spatie\Activitylog\Traits\LogsActivity`. 

On each this property `$ignoreChangedAttributes` returns an array of columns which shouldn't be logged. We can use this configuration to filter out sensitive information or any irrelevant information out of the log.

###### Fetch activity for any model

We can access change log for any model by hitting this api endpoint `api/activities/logs`.  This endpoint is completely decoupled so we can just pass through the model id & type. And it will return paginated set of change log. More details on this can be found on endpoint details.