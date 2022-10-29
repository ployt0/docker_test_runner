# docker_test_runner

A docker container amenable to being tested, as a web and SSH server, by a github workflow.

The workflow is based on a python one.

A playbook is provided to demonstrate provisioning, and by extension SSH, working.

dhparam is provided but should not be used in production, that should be evident by the "local host branch", only, in the playbook. If you have the time you must generate your own dhparam:

> openssl dhparam -out /etc/nginx/dhparam.pem 4096

