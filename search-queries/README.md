# search-queries

Exposes functions that build Gobbldygook search queries.

## Api

### `buildQueryFromString`
Given a string, returns the search query object for that string.

### `checkCourseAgainstQuery`
Given a course and a query object, returns if the course matches the query.

### `queryCourses`
Given a list of courses and a query object, filters the list of courses to only those that match.


> These two will either go back into @gobbldygook/web or will go into yet another package.
>
> - queryTreoDatabase
> - treoBatchGet
