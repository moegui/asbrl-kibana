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
- XPACK_SECURITY_ENABLED: "false"
- ES_USERNAME: 'elastic'
- ES_PASSWORD: ''
- DOCKER_NETWORK_MODE: "bridge"
- DOCKER_LOG_DRIVER: "json-file"
- DOCKER_LOG_OPTIONS: "{}"
- IMAGE: "docker.elastic.co/kibana/kibana"
- BUILD: "7.9.1"
- CONTAINER_NAME: "kibana"
- DOCKER_CPU_PERIOD: 0
- DOCKER_MEMORY: 0
- DOCKER_LABELS:
    tag1: test

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