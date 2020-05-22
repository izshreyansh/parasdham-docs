# Create new permission

1. First create a permission's entry in `permissions` table with `guard_name` set to `api`. <br>
   :information_source: Update this entry in `parasdham\database\seeds\PermissionSeeder.php` for future references.

2. Assign this permission to at least one role. You can do so by updating an entry on `role_has_permissions` table.

3.  At this point you're all set in-order to make use of new permission.<br> On the backend, You can do so with this snippet `auth()->user()->can('active-sessions')`

4. On the frontend you'll want to create a gate for this permission.
   Head over to `Parasdham-Vue\src\gates.js` file.

5. Define a new GatePolicy & pass it to `const AllGates` in the same file.

6. Head over to the page you want to put this gate on, Here's snippet that will help `$can('activeSessions', 'dashboard')` where dashboard is the key of the policy defined on previous step.
