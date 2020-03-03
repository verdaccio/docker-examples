# Docker + Kubernetes Examples

![alt verdaccio](https://cdn.verdaccio.dev/logos/verdaccio@2x.png "verdaccio devops")

[![docker pulls](https://img.shields.io/docker/pulls/verdaccio/verdaccio.svg?maxAge=43200)](https://verdaccio.org/docs/en/docker.html)
[![backers](https://opencollective.com/verdaccio/tiers/backer/badge.svg?label=Backer&color=brightgreen)](https://opencollective.com/verdaccio)
[![stackshare](https://img.shields.io/badge/Follow%20on-StackShare-blue.svg?logo=stackshare&style=flat)](https://stackshare.io/verdaccio)
[![discord](https://img.shields.io/discord/388674437219745793.svg)](http://chat.verdaccio.org/)

[![Twitter followers](https://img.shields.io/twitter/follow/verdaccio_npm.svg?style=social&label=Follow)](https://twitter.com/verdaccio_npm)
[![Github](https://img.shields.io/github/stars/verdaccio/verdaccio.svg?style=social&label=Stars)](https://github.com/verdaccio/verdaccio/stargazers)


The objective of this repository is to hold the most common configuration for `verdaccio` for different use cases in **Docker**.

> Feel free to contribute whether you consider any use case is relevant for the public in general.

## Examples

The following examples aim to be demonstrative and can be either improved or updated.

### Docker

#### Proxies

* [Docker + Apache + Verdaccio](apache-verdaccio/README.md)
* [Docker + Nginx + Verdaccio](reverse_proxy/nginx/README.md)
* [Docker + https-portal Example](https-portal-example/README.md)

#### Plugins

* [Docker + Uplinks Multi Registry](multi-registry-uplink/README.md)
* [Docker + Local Storage](docker-local-storage-volume/readme.md)
* [Docker + External Plugins](docker-plugin-external/README.md)

#### Auth

* [Docker + LDAP (OpenLDAP) Server + Verdaccio 3](ldap-verdaccio/readme.md)
* [Docker + LDAP (OpenLDAP) Server + Verdaccio 4](ldap-verdaccio-v4/readme.md) by **@kopax**
* [Docker + Gitlab](gitlab-verdaccio/README.md)
* [Docker + Active Directory](https://github.com/Mateus-Oli/verdaccio-ad-docker)


#### Storage

* [Docker + AWS S3 Plugin(localstack) + Verdaccio 4](amazon-s3-docker-example/v4/README.md)
* [Docker + AWS S3 Plugin(localstack)  + Verdaccio 3](amazon-s3-docker-example/v3/README.md)
* [Docker + Minio](https://github.com/barolab/verdaccio-minio/tree/master/example)

### Kubernetes

* Kubernetes (minikube) + Verdaccio (Basic Configuration)
* Kubernetes Helm and Verdaccio Chart (Basic Tutorial)

![alt verdaccio](https://www.verdaccio.org/img/devops_support_grey.png "verdaccio devops")


### External

* [
Verdaccio examples for Google Cloud and K8s setups. https://github.com/papezt/verdaccio-examples](https://github.com/papezt/verdaccio-examples)


### Articles

* [https://medium.com/@tompape/kubernetes-private-npm-registry-fb5f450fa611](https://medium.com/@tompape/kubernetes-private-npm-registry-fb5f450fa611)
* [Déployer Verdaccio sur rancher avec un helm](https://tommygingras.com/deployer-verdaccio-sur-rancher-avec-un-helm/)
