---
title: Rest parameters
path: /how
focus: /src/routes/[path]/+page.svelte
---

To match an unknown number of path segments, use a `[...rest]` parameter, so named for its resemblance to [rest parameters in JavaScript](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions/rest_parameters).

Rename `src/routes/[path]` to `src/routes/[...path]`. The route now matches any path.

> [!NOTE] Other, more specific routes will be tested first, making rest parameters useful as 'catch-all' routes. For example, if you needed a custom 404 page for pages inside `/categories/...`, you could add these files:
>
> ```tree
> src/routes/
> ├ categories/
> │ ├ animal/
> │ ├ mineral/
> │ ├ vegetable/
> +++│ ├ [...catchall]/
> │ │ ├ +error.svelte
> │ │ └ +page.server.js+++
> ```
>
> Inside the `+page.server.js` file, `error(404)` inside `load`.

Rest parameters do _not_ need to go at the end — a route like `/items/[...path]/edit` or `/items/[...path].json` is totally valid.
