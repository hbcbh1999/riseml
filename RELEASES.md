# RiseML v1.0.0 (2017/12/19)

This marks our 1.0.0 release 🎊🎉. We focused on making this release more stable and fixed many smaller bugs and messages compared to the previous version.
There are two major improvements.
First, RiseML now makes use of Kubernetes' persistent volume claims for its `data` and `output` volumes.
This tighter integration allows using any of the storage types that are supported in Kubernetes.
Second, we now provide a quick installer, which spins up a complete RiseML cluster (including GPU nodes) on AWS for you.
All you need is an AWS account and you're good to go in 15 minutes!

## Installation
To install RiseML, follow the [installation guide](http://docs.riseml.com/install).
New in this release is a simple installer that spins up a complete RiseML cluster on AWS for you.
Check out our [quick setup instructions](http://docs.riseml.com/install/quicksetup.html).

## Release Notes
- Reworked storage integration with Kubernetes
- Quick installer for AWS
- Improved error reporting
- Enable support for different plans: basic, professional
- Fixed `riseml init`
- Fixed Tensorboard links with latest Tensorflow versions
- Many minor UX improvements (messages, command flags, ...)

## Upgrading from Version v0.8.0

Before upgrading:
- backup your existing data volumes
- make sure to prepare `data` and `output` Kubernetes volumes as described in our [documentation](http://docs.riseml.com/install/kubernetes.html#persistence)
- remove the options `data` and `output` from you installation configuration (usually `riseml-config.yml`)
- verify the configuration options in `riseml-config.yml` are still valid since they will be applied again (e.g., if you changed the account key to a different one it will be set to the one in `riseml-config.yml`)

To update to the newest version:
```
helm update riseml
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
