## {my-site} Settings Reference

This file is a simple template for creating a credential list for your site for quick reference.

Replace all instances of {my-site} with your site's name.

Also see: [**Default Credentials**](https://varyingvagrantvagrants.org/docs/en-US/default-credentials/) on VVV GitHub page

### {my-site} Site vvv-custom.yml Settings

See full [VVV config file docs](https://varyingvagrantvagrants.org/docs/en-US/vvv-config/) for more info on these options.

```yaml
---
sites:
  #wordpress-default:
  # Don't need to include default WordPress site entries.
  my-site:
    repo:
    hosts:
      - {my-site}.dev

# Optionally include general VVV settings below if needed:
vm_config:
  memory: 1024
  cores: 1

utility-sources:
  core: https://github.com/Varying-Vagrant-Vagrants/vvv-utilities.git

utilities:
  core:
    - memcached-admin
    - opcache-status
    - phpmyadmin
    - webgrind
    - php71
```
