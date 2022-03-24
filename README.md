# supernode


## About

A small helper program for providing Node.js environments to development
sandboxes and CI systems.


## Synopsis

```shell
# Setup modern Node.js environment.
source /dev/stdin <<<"$(curl -s https://raw.githubusercontent.com/cicerops/supernode/main/supernode)"
```


## Usage

To provision and activate a corresponding Node.js environment and provide it to
your programs, run those commands upfront before invoking any other project
tasks like Makefile targets.

The programs `node`, `npm`, `npx` and `yarn` will be transparently available to
subsequent commands within the shell environment.

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
# Setup Node.js environment defined by specific software versions.
source /dev/stdin <<<"$(curl -s https://raw.githubusercontent.com/cicerops/supernode/main/supernode)"
```


## Example output

```text
---------------
supernode setup
---------------
Provisioning Node.js 14.19.1, NPM 6.14.15 and Yarn 1.22.18.

Lalala....

----------------
supernode status
----------------
Node.js: v14.19.1
NPM:     6.14.15
Yarn:    1.22.18
```


## Details

The whole machinery will be installed into a folder called `.venv` within the
working directory. The good thing is that this environment is completely
isolated from the operating system's Node.js installation.

The tools behind this installation flavor are [Python virtual environments]
and [Node.js virtual environments].


[Python virtual environments]: https://docs.python.org/3/tutorial/venv.html
[Node.js virtual environments]: https://pypi.org/project/nodeenv/
