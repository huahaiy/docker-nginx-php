# docker-nginx-php

Run nginx Web server with PHP composer and other common libraries installed. The goal is to serve as a part of local development environment for PHP based Web sites, such as Drupal.

A host directory that contains at least one valid nginx site configuration file needs to be mounted on `/etc/nginx/sites-enabled`, e.g. `-v /whatever/on/host:/etc/nginx/sites-enabled`

Three ports, 80, 8080, and 8081 are exposed. In the configuration file, at least one nginx server should listen to one of the ports. One of them should also be mapped to a host port to enable access to the site, e.g. `-p 80:80`
