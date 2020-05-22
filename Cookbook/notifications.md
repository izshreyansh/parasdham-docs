# Notifications
Notifications are currently only used in-order to send OTP to members. This functionality follows 1st party support from [Laravel Notifications](https://laravel.com/docs/7.x/notifications#introduction).

For modifications to OTP Sending functionality you can consult `App\Notifications\SendOtp` class. It uses multiple channels to send OTP notifications. 
We're using `Database` channel in order to keep a count of Otps sent to the user. You can modify notification channels on the same file at `via` function by modifying the array it returns.

###### Additional Channels
By making use of this [3rd Party](https://laravel-notification-channels.com/twilio/#installation) package, We can add support for many notification channels like: Twitter, Facebook, Trello, Intercom. Please refer the full documentation for easy coookbook.

