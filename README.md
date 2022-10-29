# docker_test_runner

![python-app workflow](https://github.com/ployt0/docker_test_runner/actions/workflows/python-app.yml/badge.svg)

A minimal docker container amenable to being tested, as a web and SSH server, by a github workflow.

The workflow is based on a python one.

A playbook is provided to demonstrate provisioning, and by extension SSH, working.

dhparam is provided but should not be used in production, that should be evident by the "local host branch", only, in the playbook.

You must generate your own dhparam before building locally, if intending for production:

> openssl dhparam -out /etc/nginx/dhparam.pem 4096

Obviously the local branch of the playbook would need to be replaced, or you can finish provisioning without a playbook.

This is a minimal microservice to present an NGINX server such as might be found in production, i.e. with SSH access and some form of TLS. Here you can test it safely.
