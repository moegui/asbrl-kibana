ASBRL-KIBANA
=========

Deploy Kibana as a Docker container.

Requirements
------------

Need to be Docker engine installed.

Role Variables
--------------

- default_user: 'ubuntu'
- HOSTNAME: 'es-kibana'
- ES_HOST: 'http://localhost:9200'
- DOCKER_NETWORK_MODE: "bridge"
- DOCKER_LOG_DRIVER: "json-file"
- DOCKER_LOG_OPTIONS: "{}"
- IMAGE: "docker.elastic.co/kibana/kibana"
- BUILD: "7.9.0"

Dependencies
------------

None

Example Playbook
----------------

      - name: Deploy Kibana
        include_role:
          name: asbrl-kibana
        vars:
          DOCKER_NETWORK_MODE: "host"

License
-------

BSD

Author Information
------------------

Moegui.com