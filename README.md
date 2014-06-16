# blog-deploy
===========

CoreOS units to deploy jekyll blog with vulcand proxy 

## Pre-requisites
1. CoreOS Cluster

## Start
For testing

1. etcdctl set "/vulcand/hosts/blog.firefight.io/locations/home/path" '/.*'
2. fleetctl start blog-*
3. fleetctl start vulcan.service

## TODO
* Add webhooks to call when git commit or docker index build
* Add rolling update script(s)
* Add quick switch over scripts
* Add ability to version control, instead of v1 use git commit id
* Use docker provided port instead of hardcoded for nginx
