# Relationships
Our most important model `App\Models\Member` has `relationships` defined on it, Which enables us to store Related Member information. In other words: Family tree information. How a given member is related to another member in the family tree.

###### Schema
Two member relationships are stored on intermediate table: `member_has_relationships`.  Each row will have pivot data column called `member_relationship_name`. It's the relationship name from base model to related model.

For example:
`member_has_relationships`

| member_id |member_relationship_name | related_member_id |
| --------- | ----------- | ------------- |
| 1         | Husband     | 2     |

Above row tells us that Member with id: 2 is `husband` of member with id: 1.

###### Frontend
We depend on front-end to provide us proper relationship mappings at the time of storing a new member / relationship. You can modify these mappings at `\src\router\datasets\RelationshipDataClass.js`. 
> The array contains forward/reverse relationships names in key called `value`.  And  Its display name is stored in array key called: `name`.

Example: 
`{value:'Son,Mother', name:'Son -> Mother'},`.

The backend will break apart these relationship combination to correctly put relationship names between members.<br /> 
You'll find this logic at `app\Actions\MemberRelationshipsSync.php@attachRelatives`.
