# agntn Renovate preset

Shared Renovate config for agntn packages. Other repos inherit it. They do not copy it.

```json
{
  "$schema": "https://docs.renovatebot.com/renovate-schema.json",
  "extends": ["local>agntn/_renovate"]
}
```

`local>` is the form that belongs here. This repo is private, so the Renovate app has to be able to read it. `github>agntn/_renovate` loads the same `default.json`.

## What you get

Pins everything except peer ranges. Waits 3 days after an npm release before it opens a PR. That delay is boring and I want it.

Patches automerge after CI. Minors land in one PR on Monday morning, Warsaw time. Majors sit on the Dependency Dashboard until somebody checks the box.

`@oh-my-pi/*` and `@earendil-works/*` stay in their own PRs. Same for icon sets (`@iconify-json/*`), oxlint, Vitest, GitHub Actions, and the `packageManager` field. One PR per host SDK, not twenty.

Do not run Dependabot version updates next to this. Alerts for vulnerabilities can stay.

## Files

- `default.json` is the preset other repos extend
- `renovate.json` is this repo extending itself

## License

[MIT](./LICENSE)
