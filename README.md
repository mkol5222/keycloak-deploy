## Keycloak playground

# local-scenario based on https://github.com/oauth2-proxy/oauth2-proxy/tree/master/contrib/local-environment

* pre-configured Keycloak
* application exposed with authentication using oauth2-proxy


### Usage

```bash
cd local-scenario
# sudo service docker start
# wsl
docker-compose up -d
```

### Test flow

* Access http://oauth2-proxy.localtest.me:4180 to initiate a login cycle using user=admin@example.com, password=password
* Access http://keycloak.localtest.me:9080 with the same credentials to check out the settings
* Logout can be done too: http://oauth2-proxy.localtest.me:4180/oauth2/sign_out

### Cleanup

```bash
docker-compose down
```