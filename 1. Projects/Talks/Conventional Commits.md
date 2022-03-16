

## The issue with commit -m 

git commit -m "<write something here to make this work.>"

## What are Conventional commits?

A lightweight convention on top of commit messages that provides a simple set of rules to create a commit history readable by both humans and machines.

## How does cc fix that?

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
- Scope: can be set to anything to provide additional contextual information

## More examples:

### Commit messages with no body

`ci: fix build pipeline`

### Commit message with scope

`feat(date-parser): add ability to parse DMY dates`
`fix(Mod-963): remove uneccessary re-renders in table component`

### Commit message with breaking change

```
chore!: drop support for Node 6

BREAKING CHANGE: use JavaScript features not available in Node 6.
```

Revert commit messages

```
revert: let us never again speak of the noodle incident

Refs: 676104e, a215868
```

## What is it for?

- Readable commit history
- Automatically generating CHANGELOGs
- Automatically determining a semantic version bump
- Better consitency + communication overall

## How we use it at Metamaze Fullstack?

Metamaze UI

![[Screenshot 2022-03-16 at 10.01.37.png]]

![[Screenshot 2022-03-16 at 10.00.58.png]]

![[Screenshot 2022-03-16 at 10.09.21.png]]
![[Screenshot 2022-03-16 at 10.13.02.png]]![[Screenshot 2022-03-16 at 10.14.35.png]]

![[Screenshot 2022-03-16 at 10.14.52.png]]
![[Screenshot 2022-03-16 at 10.11.57.png]]



![[Screenshot 2022-03-16 at 10.12.23.png]]

## Other tooling

### IDE

![[Screenshot 2022-03-16 at 10.19.10.png]]
![[Screenshot 2022-03-16 at 10.20.04.png]]

### Hooks
- JS: Husky & Commitlint
- Python: Pre-commit & Commitizen
- Other, check https://www.conventionalcommits.org/en/about/

### Automatic changelogs / releases
- lerna
- git-changelog
- standard-version
- semantic-version
- python-semantic-release


And more on: https://www.conventionalcommits.org/en/about/

## Wrap up
- Write consistent, complete commit messages
- Automate more with commit messages
- Use existing tooling for changelogs, releases, commit prompts, linters

## Thanks

Sources: 
- https://www.conventionalcommits.org/
- @marioebl's talk about the The perks of committing with conventions