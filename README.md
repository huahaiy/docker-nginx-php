# docker-nginx-php

Run nginx Web server with PHP composer and other common libraries installed. The goal is to serve as a part of local development environment for PHP based Web sites, such as Drupal.

A host directory that contains the site content needs to be mounted on `/docroot`, e.g. `-v /myhome/html:/docroot`

A host directory that contains at least one valid nginx site configuration file needs to be mounted on `/etc/nginx/sites-enabled`, e.g. `-v /myhome/nginx:/etc/nginx/sites-enabled`. 

The nginx configuration file should be configured to use `/docroot` as the document root.

Three ports, 80, 8080, and 8081 are exposed. In the configuration file, at least one nginx server should listen to one of the ports. One of them should also be mapped to a host port to enable access to the site, e.g. `-p 80:80`
