# Import & Export

This page lays out guide on import/export functionality for members.

### Import

###### Basic Usage

All of import logic is stored inside `app/Imports/MembersImport` class.
Constant array `DB_COLUMNS` returns all valid `importable` column list. <br />
Each key in `DB_COLUMNS` is passed through the `ucwords()` function, It converts the first character of each word in a string to uppercase. Thereforce our code expects csv file to have `First Name` (`first_name`) in the header key.

Import logic is independent of file format. User can upload .csv, .tsv, .html files to import from. Each row of .csv will be passed to `onRow` function of `app/Imports/MembersImport` class. Therefore you can access values from .csv file by accessing key from `$row`.

example:

`Members.csv`

| First Name | Last Name |
| -------- | -------- |
| John     | Doe  |
| Johnyy   | Bravo  |

If we import this file then we can access the value `John` at `app/Imports/MembersImport@onRow` like this: `$row['first_name']`.

We can easily mark any column as optional by using null coalescing operator.

###### Find duplicates
From `app/Imports/MembersImport` import class we'll try to reduce data duplication. It is achieved by calling `getDuplicates` on `Models/Member` model class. It will run a fuzzy search using `TNTSearch` Full text search driver.

### Export

###### Basic Usage
All of export logic is stored inside `App/Exports/MembersExport` class. We'll receive `columns`, `filters` & `fileFormat` from frontend.

We'll use `columns` to select columns & `filters` to select data sets. How to use this functionality is explained in `Filters & Sort` page in this documentation.

There 2 main parts to understand how export functionality works:

1. We run data fetch query with `dataset` function on `App/Exports/MembersExport` class.
2. We use `view` function on the same file to format our response in appropriate format. (1 row => 1 eloquent model).
