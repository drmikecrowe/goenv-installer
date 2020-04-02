# goenv installer & doctor scripts

## IMPORTANT NOTE:

This is a very quick port of [rbenv-installer](https://github.com/rbenv/rbenv-installer) for [goenv](https://github.com/syndbg/goenv).

It has only been tested in linux, and in a limited fashion. However, the only changes are search/replace (`rbenv` -> `goenv`, etc), so it should be reasonably safe.

## goenv-installer

The `goenv-installer` script idempotently installs or updates goenv on your
system. If Homebrew is detected, installation will proceed using `brew install/upgrade`. Otherwise, goenv is installed under `~/.goenv`.

Additionally, [go-build](https://github.com/syndbg/go-build#readme) is also
installed if `goenv install` is not already available.

```sh
# with curl
curl -fsSL https://github.com/drmikecrowe/goenv-installer/raw/master/bin/goenv-installer | bash

# alternatively, with wget
wget -q https://github.com/drmikecrowe/goenv-installer/raw/master/bin/goenv-installer -O- | bash
```

## goenv-doctor

After the installation, a separate `goenv-doctor` script is run to verify the
success of the installation and to detect common issues. You can run
`goenv-doctor` on your machine separately to verify the state of your install:

```sh
# with curl
curl -fsSL https://github.com/syndbg/goenv-installer/raw/master/bin/goenv-doctor | bash

# alternatively, with wget
wget -q https://github.com/syndbg/goenv-installer/raw/master/bin/goenv-doctor -O- | bash
```
