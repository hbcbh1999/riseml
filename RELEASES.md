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
