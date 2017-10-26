# RiseML

<img src="https://cdn.riseml.com/img/banner_github.png" />

[RiseML](https://riseml.com) is a scalable deep learning environment for GPU servers based on [Kubernetes](https://kubernetes.io)

This repository contains the [central issue tracker](https://github.com/riseml/riseml/issues) for the RiseML
project.

## Quick Start

You need a Kubernetes cluster up and running with ```kubectl``` and ```helm``` installed.

```
kubectl create namespace riseml
helm repo add riseml-charts https://cdn.riseml.com/helm-charts
helm install riseml-charts/riseml --name riseml --namespace riseml
```

## Documentation

Documentation for the RiseML project can be found at
<http://docs.riseml.com>.

## Other repositories

RiseML consists of many different sub-projects. The main ones are:

### riseml-xxx

xxx

### riseml-yyy

yyy

### riseml-zzz

zzz
