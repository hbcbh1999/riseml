# RiseML v1.0.0 (2017/12/19)

We are 1.0.0 finally. 

## Release Notes
- Re-worked storage integration with Kubernetes
- Quick installer for AWS
- Several fixes for better error reporting

## Upgrading from release candidates

Before upgrading:
- backup your existing data volumes
- make sure to prepare `data` and `output` Kubernetes volumes as described in our [documentation](http://docs.riseml.com/install/kubernetes.html#persistence)
- remove the options `data` and `output` from you installation configuration (usually `riseml-config.yml`)
- verify the configuration options in `riseml-config.yml` are still valid since they will be applied again (e.g., if you changed the account key to a different one it may be reset)

To update to the newest version, you can then run:
```
helm upgrade riseml-charts/riseml -f riseml-config.yml
```
If you need support with upgrading, please contact us.

# RiseML v0.8.0 (2017/11/13)

🎉 This is the first public release of RiseML!

## Installation
To install RiseML, follow the [installation guide](http://docs.riseml.com/install).

## Release Notes
- Introducing new features:
  - TensorFlow and TensorBoard support
  - Run distributed training experiments with TensorFlow
  - Run hyperparameter experiments
  - User Management
  - Monitor experiments' CPU, RAM, and GPU stats
- Improved `riseml.yml` syntax for addressing frameworks
- Improved scalability of log streaming
- Renamed `dockerBuild` installation parameter to `imageBuilder`

## Upgrading from release candidates

There is no migration path from release candidates. To upgrade, you need to completely uninstall and re-install RiseML:

1) uninstall via `helm del --purge riseml`
2) delete existing files on your database, git and log storage _(only if persistence was configured)_
3) change `dockerBuild` to `imageBuilder` in `riseml-config.yml`
4) re-install according to [installation instructions](http://docs.riseml.com/install/).
