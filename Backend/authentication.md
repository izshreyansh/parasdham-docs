# Authentication
We're making use of 1st party authentcation driver provided by laravel. [Laravel Sanctum](https://laravel.com/docs/7.x/sanctum) provides a featherweight authentication system for SPAs (single page applications), mobile applications, and simple, token based APIs.
In-order to provide forward compatibility for when we will require mobile application for this CRM. We will make use of API Token Based Authentication.

All personal access tokens are stored in `personal_access_tokens` table. We'll also store authorisation information for each token issued. Plus we'll also store `last_used_at` flag in order to keep track of stale tokens.
We'll erase our stale tokens with `tokens:clear` command, Which is set to run automatically in `console/kernel.php`.

In-order to secure routes with authentication guards, We'll make use of `auth:sanctum` middleware.

