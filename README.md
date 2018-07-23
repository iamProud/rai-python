# python bindings to rai

This is a container repo, exposing some functionality of the RAI code. See https://github.com/MarcToussaint/rai for a README of the RAI code.

## Quick Start

This assumes a standard Ubuntu 16.04 machine.

```
git clone git@github.com:MarcToussaint/rai-python.git
cd rai-python

git submodule init
git submodule update

make -j1 initUbuntuPackages  # calls sudo apt-get install; you can always interrupt
make -j4                     # builds libs and tests

source setupPython.sh
cd examples && ./basics.py

jupyter-notebook docs/1-basics.ipynb 
```

## Tutorials

Please see the [docs/](docs/) path. So far only one. The plan is:

1. [Basics:](docs/1-basics.ipynb) Configurations, Views, basic editing
1. [IK:](docs/2-constraints.ipynb) Learn about the language to set optimization constraints, first with just Inverse Kinematics; grabbing results
1. [KOMO:](docs/3-KOMO.ipynb) Interface to KOMO, the motion optimization method; learn to set constraints
1. [LGP:](docs/4-LGP.ipynb) The low-level skeleton interface to solving LGP problems
1. [Contacts:](docs/8-contacts.ipynb) Access to various methods to compute detailed collision geometries or compute stable force/wrench configurations, all static
1. [Physx:](docs/9-physx.ipynb) Access to the Physx physicsl simulation engine
1. [Bullet:](docs/10-bullet.ipynb) Access to the Physx physicsl simulation engine

## Examples

Check the [examples/](examples/) path

## Older/messy docs

Just as a reference: https://github.com/MarcToussaint/rai-maintenance/tree/master/help
