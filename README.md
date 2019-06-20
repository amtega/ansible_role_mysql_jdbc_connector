# Amtega mysql_jdbc_connector role

This is an [Ansible](http://www.ansible.com) role to deploy MySQL JDBC connector.

## Role Variables

A list of all the default variables for this role is available in `defaults/main.yml`.

The role setups the following facts:

- mysql_jdbc_connector_latest_version: latest version of the connector available on the web. This fact is only available if you are downloading from the official MySQL site.
- mysql_jdbc_connector_jar_path: full path to the deployed jar with the connector.


## Example Playbook

This is an example playbook:

``` yaml
---
- name: msyql_jdpc_connector role sample
  hosts: localhost
  roles:  
    - amtega.mysql_jdbc_connector
  vars:
    mysql_jdbc_connector_state: present
    mysql_jdbc_connector_version: 8.0.11
    mysql_jdbc_connector_dir: /root/software    
    mysql_jdbc_connector_remove_artifact: no
```

## Testing

Tests are based on docker containers. You can setup docker engine quickly using the playbook `files/setup.yml` available in the role [amtega.docker_engine](https://galaxy.ansible.com/amtega/docker_engine).

Once you have docker, you can run the tests with the following commands:

```shell
$ cd amtega.mysql_jdbc_connector/tests
$ ansible-playbook main.yml
```

## License

Copyright (C) 2019 AMTEGA - Xunta de Galicia

This role is free software: you can redistribute it and/or modify it under the terms of:

GNU General Public License version 3, or (at your option) any later version; or the European Union Public License, either Version 1.2 or – as soon they will be approved by the European Commission ­subsequent versions of the EUPL.

This role is distributed in the hope that it will be useful, but WITHOUT ANY WARRANTY; without even the implied warranty of MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the GNU General Public License for more details or European Union Public License for more details.

## Author Information

- Juan Antonio Valiño García.
