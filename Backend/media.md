# Media
We can associate media files with member models using a simple `AddMedia` Api.

###### Basic Usage
In-order to save image, We'll pass through base64code to this elegant api.

```
$member = Member::first();
$member->addMediaFromBase64($base64code)->toMediaCollection();
```
This will store the image file in `storage/app/public` folder.

###### Retrieving Image

In-order to get member's profile image URL we can do something like this:

```
Member::first()->profile_picture;
```
It will return URL of the image.

!> :information_source: In-order to access image cross domain, Please make sure that proper CORS policy have been set & `Access-Control-Allow-Origin` is properly set on headers.

###### Image Manipulations
If there's a requirement in future to add watermarks, crop images, process responsive images. Please feel free to refer to [Laravel-MediaLibrary](https://docs.spatie.be/laravel-medialibrary/v7/converting-images/defining-conversions/).

It is as simple as adding a function on `Models/Member`model.
```
public function registerMediaConversions(Media $media = null)
{
   $this->addMediaConversion('thumbnail')
      ->width(368)
      ->height(232)
      ->sharpen(10);
}
```