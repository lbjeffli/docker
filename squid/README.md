# Squid
* uses the Docker image by `sameersbn`.
* `squid.conf` has been configured to allow authenticated access to the proxy service using a username-password pair.
* it is also configured to turn on the anonymiser (Anaoymous Proxy)

## To use
* create a new folder, `/var/lib/docker-data/squid/config`, to store the config and password files for Squid; this folder will be linked to the new Docker container. 
* create a new file to store the Squid usernames and passwords:
```
sudo touch /var/lib/docker-data/squid/config/squid_passwd
sudo chown proxy /var/lib/docker-data/squid/config/squid_passwd
```
* generate new username-password pairs:
```
sudo htpasswd /var/lib/docker-data/squid/config/squid_passwd
```
repeat to create more pairs.
* move `squid.conf` to `/var/lib/docker-data/squid/config`
