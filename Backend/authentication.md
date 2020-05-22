# Authentication & Authorisation

### Authentication
We're making use of 1st party authentcation driver provided by laravel. [Laravel Sanctum](https://laravel.com/docs/7.x/sanctum) provides a featherweight authentication system for SPAs (single page applications), mobile applications, and simple, token based APIs.
In-order to provide forward compatibility for when we will require mobile application for this CRM. We will make use of API Token Based Authentication.

All personal access tokens are stored in `personal_access_tokens` table. We'll also store authorisation information for each token issued. Plus we'll also store `last_used_at` flag in order to keep track of stale tokens.
We'll erase our stale tokens with `tokens:clear` command, Which is set to run automatically in `console/kernel.php`.

In-order to secure routes with authentication guards, We'll make use of `auth:sanctum` middleware.

### Authorisation
We can authorise users by managing user permissions and roles in the database. Each permission belongs to Role. Each user will have at least one role. For user A, He will inherit permissions from the role he is assigned.
User model makes use of `Spatie\Permission\Traits\HasRoles` trait in order to provide robust permissions management.

Here's a basic flow in-order to grant user permission through role.

First create a permission:
```
	$permissions = Permission::create(['name' => 'users-crud']);   
```

Assign this permission to a role:
```
	$role = Role::create([
		'name' => 'Maintainer',
		'guard_name' => 'api'
	]);
	
	$role->syncPermissions($$permissions);
```

Finally, assign this role to a user:
```
	$user->roles()->sync($role);
```

Now you can make use of `user-crud` guard like this:
```
/**
* Determine if the user is authorized to make this request.
*
* @return bool
*/
public function authorize()
{
	return auth()->user()->can('users-crud');
}
```