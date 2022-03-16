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


## What is it for?

- Readable commit history
- Automatically generating CHANGELOGs
- Automatically determining a semantic version bump
- Better communication overall

## How we use it at Metamaze Fullstack?

Metamaze UI

![[Screenshot 2022-03-16 at 10.01.37.png]]
![[Screenshot 2022-03-16 at 10.00.58.png]]



## Other tooling

### IDE

### Hooks

### Standard versionning
