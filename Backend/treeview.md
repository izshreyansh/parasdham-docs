# Mission's Treeview
In-order to store hierarchical data for missions, We make use of [Nested Set Model](https://en.wikipedia.org/wiki/Nested_set_model).

> The nested set model is to number the nodes according to a tree traversal, which visits each node twice, assigning numbers in the order of visiting, and at both visits. This leaves two numbers for each node, which are stored as two attributes. Querying becomes inexpensive: hierarchy membership can be tested by comparing these numbers. Updating requires renumbering and is therefore expensive.

###### Appending and prepending to the specified parent
If you want to make mission a child of other mission, you can make it last or first child.
> In following examples, $parent is some existing mission.

```
// #1 Using deferred insert
$mission->appendToNode($parent)->save();

// #2 Using parent node
$parent->appendNode($mission);

// #3 Using parent's children relationship
$parent->children()->create($attributes);

// #5 Using node's parent relationship
$mission->parent()->associate($parent)->save();

// #6 Using the parent attribute
$mission->parent_id = $parent->id;
$mission->save();
```

###### Rebuilding a tree from array
You can easily rebuild a tree. This is useful for mass-changing the structure of the tree.
```
Mission::rebuildTree($data);
```

$data is an array of missions:
```
$data = [
    [ 'id' => 1, 'name' => 'Parasdham', 'children' => 
    	[
			`id`=> 2, 'name' => 'aysg'
    	] 
   ],
];
```

###### Accessing  Ancestors and descendants

```
// Accessing ancestors
$mission->ancestors;

// Accessing descendants
$mission->descendants;
```