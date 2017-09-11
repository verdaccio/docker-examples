# Verdaccio and LDAP Server

Running `verdaccio` with the plugin [https://github.com/Alexandre-io/verdaccio-ldap](https://github.com/Alexandre-io/verdaccio-ldap).

**EXPERIMENTAL** - It does not work yet.


To run the containers, run the following command in this folder, it should starts the containers in dettach mode.

```bash
➜ docker-compose up -d
```

To recreate the nginx image you can force the build.

```bash
➜ docker-compose up --force-recreate --build
Building verdaccio
Step 1/18 : FROM node:8.4.0-alpine
 ---> 016382f39a51
Step 2/18 : LABEL maintainer "https://github.com/verdaccio/verdaccio"
 ---> Using cache
 ---> a6ddcb63eb95
Step 3/18 : RUN apk --no-cache add openssl &&     wget -O /usr/local/bin/dumb-init https://github.com/Yelp/dumb-init/releases/download/v1.2.0/dumb-init_1.2.0_amd64 &&     chmod +x /usr/local/bin/dumb-init &&     apk del openssl
 ---> Using cache
 ---> 52ba1e399e93
Step 4/18 : ENV APPDIR /usr/local/app
...
Successfully tagged ldapverdaccio_verdaccio:latest
Recreating ldapverdaccio_verdaccio_1 ... 
Recreating ldapverdaccio_verdaccio_1 ... done
Recreating ldapverdaccio_ldapserver_1 ... 
Recreating ldapverdaccio_ldapserver_1 ... done
Attaching to ldapverdaccio_verdaccio_1, ldapverdaccio_ldapserver_1
ldapserver_1  | 59b6f026 @(#) $OpenLDAP: slapd  (Ubuntu) (May 25 2015 13:12:01) $
ldapserver_1  | 	buildd@toyol:/build/buildd/openldap-2.4.31/debian/build/servers/slapd
ldapserver_1  | 59b6f026 hdb_db_open: database "dc=nodomain": unclean shutdown detected; attempting recovery.
verdaccio_1   |  warn --- config file  - /verdaccio/conf/config.yaml
ldapserver_1  | 59b6f026 hdb_db_open: database "dc=openstack,dc=org": unclean shutdown detected; attempting recovery.
ldapserver_1  | 59b6f026 slapd starting
ldapserver_1  | 59b6f026 bdb(dc=nodomain): BDB0060 PANIC: fatal region error detected; run recovery
verdaccio_1   |  warn --- http address - http://0.0.0.0:4873/ - verdaccio/2.3.6


``` 

To force recreate the images.

```bash
docker-compose up --build --force-recreate -d
```

To stop all containers

```bash
docker-compose stop
```

To display container logs

```bash
➜ docker-compose logs
Attaching to ldapverdaccio_ldapserver_1, ldapverdaccio_verdaccio_1
verdaccio_1   |  warn --- config file  - /verdaccio/conf/config.yaml
verdaccio_1   |  warn --- http address - http://0.0.0.0:4873/ - verdaccio/2.3.6
ldapserver_1  | 59b6f026 @(#) $OpenLDAP: slapd  (Ubuntu) (May 25 2015 13:12:01) $
ldapserver_1  | 	buildd@toyol:/build/buildd/openldap-2.4.31/debian/build/servers/slapd
ldapserver_1  | 59b6f026 hdb_db_open: database "dc=nodomain": unclean shutdown detected; attempting recovery.
ldapserver_1  | 59b6f026 hdb_db_open: database "dc=openstack,dc=org": unclean shutdown detected; attempting recovery.
ldapserver_1  | 59b6f026 slapd starting
ldapserver_1  | 59b6f026 bdb(dc=nodomain): BDB0060 PANIC: fatal region error detected; run recovery
```

