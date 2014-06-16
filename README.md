# blog-deploy
===========

CoreOS units to deploy jekyll blog with vulcand proxy 

## Pre-requisites
1. CoreOS Cluster

## Start

1. fleetctl start vulcan.service
2. etcdctl set "/vulcand/hosts/blog.firefight.io/locations/home/path" '/.*'
3. fleetctl start blog-*

## TODO
* Add webhooks to call when git commit or docker index build
* Add rolling update script(s)
* Add quick switch over scripts
* Add ability to version control, instead of v1 use git commit id
* Use docker provided port instead of hardcoded for nginx
