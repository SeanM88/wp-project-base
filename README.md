# wp-site-base

Boilerplate WordPress site directory for use with **Varying Vagrant Vagrants** local environments, although could easily be used in any new WordPress project where you want to track an actual WordPress website and optionally use Git for deployment.

This Git repo begins at the same level as the actual WordPress site directory, meaning the same folder that `wp-config.php`, `wp-content` directory, etc. are usually located.  

By default, it is set up to only track specific themes and plugins critical to site functionality & display by whitelisting their directories in the provided `.gitignore` file, although other folders & files can be whitelisted as desired, it is usually best practice to only track especially relevant files.

Note: the Git repo and actual directory name do not need to match; this is worth mentioning because this directory is usually named something like `public_html` or `htdocs` on most webservers and requires extra unnessary server configuration to change, so its best left as is.

You can however specify a meaningful name (e.g. mycoolwebsite) for the Git repository at other locations, for example at Git hosting sites like GitHub and Bitbucket.

## Getting Started

While **wp-project-base** can be easily adpated as a base for any new WordPress site, it was originally created for local WordPress development using Varying Vagrant Vagrants.

Therefore, directions here pertain to using this repo in combination with [VVV 2](https://github.com/Varying-Vagrant-Vagrants/VVV) + [wp-vvv2-make-site](https://github.com/SeanM88/wp-vvv2-make-site) projects.

### Prerequisites

- [**VVV 2.0**](https://github.com/Varying-Vagrant-Vagrants/VVV)
- [Vagrant::Hostsupdater](https://github.com/cogitatio/vagrant-hostsupdater) - Vagrant plugin for auto-updating system's hosts file.
- [**wp-vvv2-make-site**](https://github.com/SeanM88/wp-vvv2-make-site) - Git repo for auto-site setup in `vvv-custom.yml`

### Install

1. Clone this repo into a local directory on your computer, replacing "my-site-name" with your own site's.
`git clone https://github.com/SeanM88/wp-site-base.git my-site-name`

2. Run the following command (again replacing "my-site-name" with your own) to move to the newly created site directory and remove the existing .git subfolder — this tracks **wp-site-base**, we want to track our site in it's own repo.
`cd my-site-name && rm -Rf .git`

### Configuration

We now have a fresh and clean site directory to use with **wp-vvv2-make-site** and get started developing our site locally.  Before we can actually use it though we need to add our site's theme and any necessary plugins.

1. Copy your site's theme and required plugins into the respective `/themes/` and `/plugins/` directory inside `/wp-content/`

2. Open the `.gitignore` file and whitelist all the theme and plugin directorys you just added, using the Git [negate pattern prefix](https://git-scm.com/docs/gitignore#_pattern_format).  
   For example: `!wp-content/themes/my-site-theme/` or `!wp-content/plugins/my-plugin/`

