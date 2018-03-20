## Deploy steps
- `mix edeliver build release` will put the repo on the build server, compiles and builds
- `mix edeliver deploy release to production` it uploads that package to production server
- `mix edeliver restart production`

Server provisioning ansible script for http://loaded.bike to be hosted on DigitalOcean (Ubuntu 16.10)

`ansible-playbook provision.yml --ask-become-pass`

Note:

* After provisioning happens you can't run this again as a root user
* Run `certbot --nginx` (need to figure out auto-renew eventually)
