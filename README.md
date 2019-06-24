# net.dapla.webide
Dockerized git+ssh only webide

## Configuration

Env Name | Env Value 
- | -
EMAIL | Str(`<github user email>`)
DOMAINNAME | Str(`<dns domain name>`)
HOSTNAME |  Str(`<dns hostname>`)
TZ | Str(`Timezone`)
LC_ALL, LANG, LANGUAGE | Str(Defaults: "en_US.UTF-8", <"locale setting">)


## Additional Settings:

Use  these to configure a proxy for git/linux while on corporate networ
```
# NOTE: See https://gist.github.com/patik/6d40ded40bf93c2f381b for additonal details
# environment variables are UPPERCASE even in git bash
HTTP_PROXY="http://$USERNAME:$PASSWORD@$PROXY_SERVER:$PROXY_PORT"
HTTPS_PROXY=$HTTP_PROXY
FTP_PROXY=$HTTP_PROXY
SOCKS_PROXY=$HTTP_PROXY
GIT_SSL_NO_VERIFY=1
GIT_CURL_VERBOSE=1

NO_PROXY="localhost,127.0.0.1,$DOMAINNAME"
```
