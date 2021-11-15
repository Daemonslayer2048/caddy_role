# Anisble Server Common Role  
This roles setups up a [Caddy v2](https://caddyserver.com/) reverse proxy server.

## Requirements
### ansible-galaxy
__Collections:__
  - community.general

__Roles:__
  - daemonslayer2048.common

## Variables
| Variable | Type | Required | Default | Example |
|    -     |   -  |     -    |    -    |    -    |
|caddy_acme_ca| string | true | https://acme-staging-v02.api.letsencrypt.org/directory | https://acme-v02.api.letsencrypt.org/directory |
|caddy_email| string | true | none@null.com | none@null.com |

# Notes:
## Testing Issues
  - Selinux Modules can not be tested in podman so these tests are performed outside of the stesting suite :(
