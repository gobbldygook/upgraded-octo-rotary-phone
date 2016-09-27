# core

Pulls together and re-exports a bunch of the "core" packages into one namespace.

Packages:

- `@gobbldygook/course-conflicts`
- `@gobbldygook/examine-student`
- `@gobbldygook/expand-student`
- `@gobbldygook/schedule-builder`
- `@gobbldygook/search-queries`
- `@gobbldygook/student-format`

At the moment, I think that this can be done by simply re-exporting all of their exports from this package:

```ts
export * from '@gobbldygook/course-conflicts'
export * from '@gobbldygook/examine-student'
export * from '@gobbldygook/expand-student'
export * from '@gobbldygook/schedule-builder'
export * from '@gobbldygook/search-queries'
export * from '@gobbldygook/student-format'
```

We'll see how long that works.
