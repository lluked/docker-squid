## Docker-Squid ##

Squid proxy setup built from source within the Dockerfile, enabling build options needed for ssl bumping. The Dockerfile leaves the squid configuration as default, however, the docker-compose file mounts the configuration needed for ssl bumping.

The Squid configuration is based on the default configuration and follows the steps outlined in [SslBumpExplicit](https://wiki.squid-cache.org/ConfigExamples/Intercept/SslBumpExplicit) and [SslPeekAndSplice](https://wiki.squid-cache.org/Features/SslPeekAndSplice) to setup ssl bumping.

Certificates are created automatically on startup, myCA.pem and myCA.der are used as shown in SslBumpExplicit documentation. myCA.der should be imported as described in the documentation. 
