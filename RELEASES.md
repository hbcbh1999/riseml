# Release 0.8.0

This is the first public release of RiseML.

## Major Features
- Tensorflow and Tensorboard support
- Distributed training experiments with Tensorflow
- Hyperparameter experiments
- User management
- Monitor Experiment's CPU and GPU stats

## Upgrading

This release provides no migration path for release candidates so far.
To upgrade, you need to uninstall your existing RiseML installations and re-install.
You can use `helm del --purge riseml` to uninstall RiseML from Kubernetes.
If you configured persistence for your existing RiseML installation, make sure to delete existing files on your database, git and log storage.
Afterwards, re-install riseml as per the docs.
Beware, that in the installation parameters, `dockerBuild` was renamed to `imageBuilder`, all other configuration parameters remained.
