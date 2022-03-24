# supernode


## About

A small helper program for providing Node.js environments to development
sandboxes and CI systems.


## Synopsis

To provision and activate a corresponding Node.js environment and provide it to
your programs, run those commands upfront before invoking any other project
tasks like Makefile targets.

```shell
# Define software versions.
export NODEJS_VERSION=14.19.2
export NPM_VERSION=6.14.15
export YARN_VERSION=1.22.18

# Setup Node.js environment.
source /dev/stdin <<<"$(curl -s https://raw.githubusercontent.com/cicerops/supernode/main/init)"
```
