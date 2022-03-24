# supernode


## About

A small helper program for providing Node.js environments to development
sandboxes and CI systems.


## Synopsis

To provision and activate a corresponding Node.js environment and provide it to
your programs, run those commands upfront before invoking any other project
tasks like Makefile targets.

```shell
# Define a software environment typical for the active Node.js 16 LTS release.
export NODEJS_VERSION=16.14.2
export NPM_VERSION=8.5.5
export YARN_VERSION=2.4.3

# Define a software environment typical for the previous Node.js 14 LTS release.
export NODEJS_VERSION=14.19.1
export NPM_VERSION=6.14.15
export YARN_VERSION=1.22.18
```

```shell
# Setup Node.js environment.
source /dev/stdin <<<"$(curl -s https://raw.githubusercontent.com/cicerops/supernode/main/supernode)"
```
