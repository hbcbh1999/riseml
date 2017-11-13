# RiseML v0.8.0 (2017/11/13)

This is the first public release of RiseML.

## Release Notes
- TensorFlow and TensorBoard support
- Run distributed training experiments with TensorFlow
- Run hyperparameter experiments
- User Management
- Monitor experiments' CPU, RAM, and GPU stats
- Improved riseml.yml syntax for addressing frameworks
- Rewritten Loghandler

## Upgrading

This release provides no migration path for release candidates so far (we only provide migration paths for stable/proper releases).
To upgrade, you need to uninstall your existing RiseML installations and re-install.
You can use `helm del --purge riseml` to uninstall RiseML from Kubernetes.

If you configured persistence for your existing RiseML installation, make sure to delete existing files on your database, git and log storage.
Afterwards, re-install RiseML as per the [docs](http://docs.riseml.com/).

In the installation parameters, `dockerBuild` was renamed to `imageBuilder`, so if you used that flag, please rename it (all other configuration parameters remained).
