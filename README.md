# RecipeDatabase

Database of recipes.
For ideal experience consider opening the repository in [Obsidian](https://obsidian.md/).
Look here for a google sheet that computes ingredients based on number of portions (not public): [Ingredients](https://docs.google.com/spreadsheets/d/17TsMHgSJK_kX367CU9UGzMKYD2ffc12io5_qgkD2sjA/edit?gid=0#gid=0).
The individual recipes can be found in [./recipes/](./recipes/)

## Notes to the User
* I am currently in the process of recooking all recipes in order to attach images to each one
* not all files have been filled yet, once recooking of a certain recipe is completed, the recipe will be added
* ingredient listed with a value of 0 have the following meaning
    * quantity so small, that it does not make sense to provide a value
    * add based on your taste

## Table of Contents

```dataview
TABLE
	filter(file.outlinks, (l) => !regexmatch("^.+gfx/.+$", string(l))) AS "Outlinks"
WHERE 
	file.name != "README"
```

## TODO

- [ ] Adjust layouts to new template

```dataview
TABLE task.text AS "Task", choice(task.completed, "✅", "❌") AS "Completed"
FROM ""
FLATTEN file.tasks AS task
WHERE !task.completed or task.completed
```

```dataview
TABLE todo
WHERE todo = true
```