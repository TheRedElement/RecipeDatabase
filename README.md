# RecipeDatabase

Database of recipes.
For ideal experience consider opening the repository in [Obsidian](https://obsidian.md/).


## Table of Contents

```dataview
TABLE
	ingredients AS "Ingredients", amounts AS "Amounts (4 Portions)",
	filter(file.outlinks, (l) => !regexmatch("^.+gfx/.+$", string(l))) AS "Outlinks"
WHERE 
	file.name != "README"
```

## TODO

- [ ] Adjust layouts to new template

```dataview
TABLE todo
WHERE todo = true
```