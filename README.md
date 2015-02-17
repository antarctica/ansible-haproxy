# HA Proxy ('haproxy')

**Part of the BAS Ansible Role Collection (BARC)**

Installs the HA Proxy load balancer and reverse proxy

## Overview

* Installs HA Proxy.
* Creates HA Proxy configuration file by assembling a set of configuration files together.
* Provides a default set of configuration files which aren't useful but demonstrate the various HA concepts.
 
## Availability

This role is designed for internal use but if useful can be shared publicly.

## Usage

### Requirements

#### BAS Ansible Role Collection (BARC)

* `core`

### Variables

* `haproxy_configuration_assemble`
    * If "True" the role should assemble configuration files into a HA proxy configuration file
    * If you need to perform tasks such as templating before a configuration file can be made, set to "False"
    * Default: "True"
* `haproxy_configuration_directory`
    * Relative path to directory containing HA proxy configuration files
    * Files are relative to the `files` directory in this role
    * Files in this directory will be concatenated using a blank line as a separator
    * Files are concatenated in file order as viewed by `ls`
    * Default: "configs/defaults"

## Contributing

This project welcomes contributions, see `CONTRIBUTING` for our general policy.

## Developing

### Committing changes

The [Git flow](https://www.atlassian.com/git/tutorials/comparing-workflows/gitflow-workflow) workflow is used to manage development of this package.

Discrete changes should be made within *feature* branches, created from and merged back into *develop* (where small one-line changes may be made directly).

When ready to release a set of features/changes create a *release* branch from *develop*, update documentation as required and merge into *master* with a tagged, [semantic version](http://semver.org/) (e.g. `v1.2.3`).

After releases the *master* branch should be merged with *develop* to restart the process. High impact bugs can be addressed in *hotfix* branches, created from and merged into *master* directly (and then into *develop*).

### Issue tracking

Issues, bugs, improvements, questions, suggestions and other tasks related to this package are managed through the BAS Web & Applications Team Jira project ([BASWEB](https://jira.ceh.ac.uk/browse/BASWEB)).

## License

Copyright 2015 NERC BAS. Licensed under the MIT license, see `LICENSE` for details.
