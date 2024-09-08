Role Name
=========

A role to get docker traefik running

Requirements
------------

- docker
- ansible

Role Variables
--------------

```yaml
traefik_docker_network: "webproxy"
traefik_working_directory: "/path"
traefik_log:
  level: "info"
  format: "json"
traefik_logging:
  driver: "json-file"
  max_size: "10m"
  max_file: "3"
traefik_api:
  host: "domain"
  users:
    - "user1"
  main: "domain1"
  sans:
    - "domain2"
cloudflare:
  email: "you@mail.com"
  token: "your_token"
```

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: traefik
      roles:
         - { role: mfic.traefik }

License
-------

MIT
