## What is it?

A lightweight convention on top of commit messages that provides a simple set of rules to create a commit history readable by both humans and machines.


## What does it look like?

The specification is as follows:
- Commit messages should be structured as follows:
  
```
<type>[optional scope]: <description>

[optional body]

[optional footer(s)]
```
- Type can have one of the following values:
  - fix: for a commit that patches a bug (correlates with PATCH in semantic versioning)
  - feat: that introduces a new feature (correlates with MINOR in semver)
  - also supported: `build:`, `chore:`, `ci:`, `docs:`, `style:`, `refactor:`, `perf:`, `test:` and others
  - Breaking changes are marked using a `!` after the type/scope or by adding `BREAKING CHANGE:` to the footer. (correlated with MAJOR in semver)
- Scope: can be set to anything to provide additional contextual information e.g `feat(date-parser): `

## What is it for?

## How we use it at Metamaze?

## Recommended tooling

### IDE

### Hooks

### Standard versionning
