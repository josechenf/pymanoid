# pymanoid

Python library for humanoid robotics. Extends OpenRAVE with:

- Primitives for contacts, stances, point-mass systems, ...
- Jacobians and hessians for the center of mass, angular momentum, ...
- A whole-body  Inverse Kinematics (IK) solver based on the [weight-prioritized
  multi-task framework](https://hal.archives-ouvertes.fr/hal-01247118)
- Contact stability criteria: Contact Wrench Cone (CWC), stability polygons,
  computation of supporting contact forces, ...
- Drawing primitives for 2D and 3D polyhedra (polygons, cones, ...)
- Backends for various LP and QP solvers

## Use cases

<img src="https://scaron.info/images/ijhr-2016.png" width="350" align="right" />

- [Multi-contact Walking Pattern Generation](https://scaron.info/research/pre-print-2016-1.html)
- [Generalized ZMP support areas for multi-contact locomotion](https://scaron.info/research/arxiv-2015.html)
- [Humanoid Stair Climbing](https://scaron.info/research/ijhr-2016.html)

## Installation

- First, [install OpenRAVE](https://scaron.info/teaching/installing-openrave-on-ubuntu-14.04.html).
- Install all Python dependencies:
```
sudo apt-get install cython python python-dev python-pip python-scipy
sudo pip install quadprog pycddlib
```
- Finally, if you wish to install the library system-wide:
```
sudo python setup.py install
```

The preferred QP solver is [quadprog](https://github.com/rmcgibbo/quadprog).
Alternatively, *pymanoid* will try to use [CVXOPT](http://cvxopt.org) or
[qpOASES](https://projects.coin-or.org/qpOASES) if they are installed.

## Usage

See the [examples](/examples) folder for some sample test cases. For a more
elaborate use case, see [3d-mpc](https://github.com/stephane-caron/3d-mpc).
