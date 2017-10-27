# RiseML

<img src="https://cdn.riseml.com/img/banner_github.png" />

[RiseML](https://riseml.com) is a scalable deep learning environment for GPU servers based on [Kubernetes](https://kubernetes.io)

This repository contains the [central issue tracker](https://github.com/riseml/riseml/issues) for the RiseML
project.

## Installation

### Software Requirements

|               | Version   | Comments                |
| ------------- | --------- | ----------------------- |
| Linux kernel  | ≥ 3.10    |                         |
| Docker        | ≥ 1.12.6  |                         |
| Kubernetes    | ≥ 1.6.0   |                         |
| Helm          | ≥ 2.5     | If you use RBAC, you need to [configure permissions](http://docs.riseml.com/install/kubernetes.md#helm-setup) |
| Nvidia driver | ≥ 375     | (**Optional**) GPU only |

Follow the installation instructions at: <http://docs.riseml.com/install/>.

## Documentation

Documentation for RiseML can be found at <http://docs.riseml.com>.

## Repositories

### client

[client](https://github.com/riseml/client) contains the RiseML command line client.
It connects to the RiseML API server and allows you start and monitor experiments on your GPU cluster.

### riseml-yyy

yyy

### riseml-zzz

zzz
