# Anisble Server Common Role  
This roles setups up a [Caddy v2](https://caddyserver.com/) reverse proxy server.

## Requirements
### ansible-galaxy
__Collections:__
  - community.general

__Roles:__
  - [daemonslayer2048.common](https://github.com/Daemonslayer2048/common_role)

## Variables
| Variable | Type | Required | Default | Example |
|    -     |   -  |     -    |    -    |    -    |
|caddy_acme_ca| string | true | https://acme-staging-v02.api.letsencrypt.org/directory | https://acme-v02.api.letsencrypt.org/directory |
|caddy_email| string | true | none@null.com | none@null.com |

### Variable Summaries:
#### caddy_acme_ca  
By default the acme ca is set to the letsencrypt staging servers, when first deploying it is more likely to hit their rate limit so setting it to the testing servers prevents this from occuring.

#### caddy_email
The email lets encrypt should contact for issues.

# Notes:
## Testing Issues
  - Selinux Modules can not be tested in podman so these tests are performed outside of the stesting suite :(
