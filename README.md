# wp-project-base

Quick boilerplate WordPress site directory for use with Varying Vagrant Vagrants local environments, although could easily be used in any new WordPress project where you want to track an actual WordPress website and optionally use Git for deployment.

This Git repo begins at the same level as the actual WordPress site directory, meaning the same folder that `wp-config.php`, `wp-content` directory, etc. are usually located.

Note: the Git repo and actual directory name do not need to match; this is worth mentioning because this directory is usually named something like `public_html` or `htdocs` on most webservers and requires extra unnessary server configuration to change, so its best left as is.

You can however specify a meaningful name (e.g. mycoolwebsite) for the Git repository at other locations, for example at Git hosting sites like GitHub and Bitbucket.

## Getting Started

While **wp-project-base** can be easily adpated as a base for any new WordPress site, it was originally created for local WordPress development using Varying Vagrant Vagrants.

Therefore, directions here pertain to using this repo in combination with [VVV 2](https://github.com/Varying-Vagrant-Vagrants/VVV) + [wp-vvv2-make-site](https://github.com/SeanM88/wp-vvv2-make-site) projects.

### Prerequisites

* [**VVV 2.0**](https://github.com/Varying-Vagrant-Vagrants/VVV)
* [Vagrant::Hostsupdater](https://github.com/cogitatio/vagrant-hostsupdater) - Vagrant plugin for auto-updating system's hosts file.
* [**wp-vvv2-make-site**](https://github.com/SeanM88/wp-vvv2-make-site) - Git repo for auto-site setup in `vvv-custom.yml`

### Install

1. 

