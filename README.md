# linalg

![PyPI](https://img.shields.io/pypi/v/linalg.svg)
[![Documentation Status](https://readthedocs.org/projects/linalg/badge/?version=latest)](https://linalg.readthedocs.io/en/latest/?badge=latest)
![PyPI - Downloads](https://img.shields.io/pypi/dm/linalg.svg)

## Installation

Installation can be done through `pip`. You must have python version >= 3.6.

    pip install linalg

## Docs

Docs can be found at the [readthedocs page](https://linalg.readthedocs.io/en/latest/)

## What is this?

NOT intended to be the best or fastest.

NOT intended to be production-grade (yet).

IS intended to be fully vanilla python3.

IS meant as an educational tool.

## Technical details

This package uses [black](https://github.com/python/black) for formatting and [semver](https://semver.org/) for versioning.

## Usage

This package provides the `Matrix` class and utility functions.

    import linalg
    from linalg import *  # import the Matrix class and utility functions top-level
    from linalg import Matrix  # import the Matrix class

To create a matrix object, initialize it with a 2D list or use `Matrix.zeroes()` or `Matrix.identity()`. You can also use `random_matrix()`.

    mat = linalg.Matrix([[3, 4, 5], [2, 5, -1], [0, 2, 1]])  # 3x3 matrix
    mat = linalg.as_matrix([[3, 4, 5], [2, 5, -1], [0, 2, 1]])  # 3x3 matrix, alternative notation
    mat = linalg.zeroes(4, 2)  # 4x2 zero matrix
    mat = linalg.identity(4)  # 4x4 identity matrix
    mat = linalg.random_matrix((2, 3), (-10, 10))  # 2x3 matrix with elements within (-10, 10)

This package implements matrix multiplication with the python matrix multiplication operator `@` (`__matmul__`). The matrix multiplication of two `linalg.Matrix` A, B is `C = A @ B`.

After that, you can use multiple functions to perform linear algebraic operations as explained in the above linked docs.

## Todo

- [ ] Add other linear algebraic operations
- [ ] Implement vectors
- [ ] Add documentation
