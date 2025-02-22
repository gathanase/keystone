## Base Project - Custom IDs

This base project implements expands on the [Task Management](/examples/usecase-todo) example to demonstrate the use of custom string `id` fields.

We use the standard `Task` and `People` lists but, in addition, both lists:

- Specify `db: { idField: { kind: 'string' } }` to enable arbitrary string ids
- Implement a `resolveInput` hook that generates `id` values in a custom format on create

In this case the id format is `${listKey}_${cuid2()}` (eg. `TASK_knu49p0kr0m9p7q79goxgrnh` or `PERSON_bpr7cdktsykgf486cmvqmfq1`) but any string format could be used.
If the `resolveInput` was exclude, the id fields would fall back to using standard `cuid` values – the Keystone default.

## Instructions

To run this project, clone the Keystone repository locally, run `pnpm install` at the root of the repository then navigate to this directory and run:

```shell
pnpm dev
```

This will start Keystone’s Admin UI at [localhost:3000](http://localhost:3000), where you can add items to an empty database.

You can also access Keystone’s GraphQL Playground at [localhost:3000/api/graphql](http://localhost:3000/api/graphql) to explore the GraphQL API, and run [queries](https://keystonejs.com/docs/guides/filters) and [mutations](https://keystonejs.com/docs/graphql/overview#mutations) on your data.

Congratulations, you’re now up and running with Keystone! 🚀

### Optional: add sample data

This example includes sample data. To add it to your database:

1. Ensure you’ve initialised your project with `pnpm dev` at least once.
2. Run `pnpm seed-data`. This will populate your database with sample content.
3. Run `pnpm dev` again to startup Admin UI with sample data in place.

## Next steps

Experiment with the code in this example to see how Keystone works, familiarise yourself with the Admin UI, and learn about the GraphQL Playground.

When you’ve got the hang of this base project, try a [feature project](../) to learn Keystone’s advanced features and take your knowledge to the next level.

## Try it out in CodeSandbox 🧪

You can play with this example online in a web browser using the free [codesandbox.io](https://codesandbox.io/) service. To launch this example, open the URL <https://githubbox.com/keystonejs/keystone/tree/main/examples/custom-ids>. You can also fork this sandbox to make your own changes.
