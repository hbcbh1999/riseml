# RiseML

<img src="https://cdn.riseml.com/img/banner_github_blueprint.png" />

[RiseML](https://riseml.com) is a deep learning platform for [Kubernetes](https://kubernetes.io)

This repository contains the [central issue tracker](https://github.com/riseml/riseml/issues) for RiseML.

## Installation

The latest version of RiseML is v1.0.1. See the [release notes](RELEASES.md#riseml-v101-20171220) for details and upgrading.

### Software Requirements

|               | Version   | Comments                |
| ------------- | --------- | ----------------------- |
| Linux kernel  | ≥ 3.10    |                         |
| Docker        | ≥ 1.12.6  |                         |
| Kubernetes    | ≥ 1.6.0   |                         |
| Helm          | ≥ 2.5     | If you use RBAC, you need to [configure permissions](http://docs.riseml.com/install/kubernetes.html#helm-setup) |
| NVIDIA driver | ≥ 375     | (**Optional**) GPU only |

Follow the installation instructions at: <http://docs.riseml.com/install/>.

Installing Kubernetes and RiseML from scratch (Screencast, 45min):

[![IMAGE ALT TEXT](http://img.youtube.com/vi/7GU1Z6TFtA0/0.jpg)](http://www.youtube.com/watch?v=7GU1Z6TFtA0 "Installing Kubernetes and RiseML from scratch")

## Documentation

Documentation for RiseML can be found at <http://docs.riseml.com>.

## Repositories

### [riseml/monitor](https://github.com/riseml/monitor)

The RiseML monitor publishes utilization stats and node information for Kubernetes nodes and PODs.
This includes GPU information and statistics like available NVIDIA driver version, installed GPUs with serial number/model/type, current  usage and temperature.

### [riseml/cli](https://github.com/riseml/cli)

The RiseML command line client connects to the RiseML API server and allows you start and monitor experiments on your GPU cluster.

### [riseml/config-parser](https://github.com/riseml/config-parser)

The RiseML config parser validates and parses the RiseML experiment configurations (`riseml.yml`).
It is used by the client and server for validation and can easily be incorporated in other libraries.

### [riseml/client-python](https://github.com/riseml/client-python)

The RiseML Python library allows you to report results of experiments from your Python code.

### [riseml/examples](https://github.com/riseml/examples)

Several example projects to run and test your RiseML GPU cluster.
