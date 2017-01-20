# Tagging commits

Using a few sane (for my use-case) defaults like signed tags (`-s`), no messages (`-m ''`) and a simple version string, it comes down to this:

Use the following to tag the latest commit with the semver version `1.2.3`.

```shell
git tag -s -a 1.2.3 -m ''
```

Use the following to tag a specific commit (`dd4a990`) with the semver version `1.2.3`.

```shell
git tag -s -a 1.2.3 dd4a990 -m ''
```
