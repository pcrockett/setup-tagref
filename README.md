# setup-tagref action

easy way to install [tagref](https://github.com/stepchowfun/tagref) in your GitHub
Actions workflows.

```yaml
jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@9c091bb21b7c1c1d1991bb908d89e4e9dddfe3e0  # v7.0.0
      - uses: pcrockett/setup-tagref@LATEST_RELEASE_TAG
```

if you don't want to use the default version of tagref that comes with this action, you
can specify your own version and checksum:

```yaml
- uses: pcrockett/setup-tagref@LATEST_RELEASE_TAG
  with:
    version: '1.13.0'
    checksum: '59b62982784ea3f54fa8dd5869ff7bb9cff8adec7b7ab6315ae5110102e3bc7e'
```

**recommended:** run [pinact](https://github.com/suzuki-shunsuke/pinact) to pin your
actions to a specific release. don't worry, if you're using Dependabot, Renovate, etc.,
they will update your pins correctly for you.

```bash
pinact run --update
```
