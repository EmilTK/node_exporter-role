node_exporter-role
=========

This role installs node_exporter on Linux servers with a self-signed TLS certificate and BaseAuth authentication.
Functionality will be added to install additional exporters (windows, nginx).

Requirements
------------

Ansible > 2.9

Role Variables
--------------

  variable | Description | Default
 --- | --- | ---
 ne_version | Node exporter package version | 1.5.0
 ne_arch | System architecture | amd64
 ne_port | Node exporter port | 9100
 ne_bin_path |node_exporter binary file path | /opt/node_exporter
 cert_path |Node exporter certificates path| {{ ne_bin_path }}/certs
 prometheus_user | Prometheus user for Basic Auth | ""
 prometheus_password |Prometheus password for Basic Auth | ""
 prometheus_password_hash | Prometheus hash password for Basic Auth| ""


Example Playbook
----------------

    - name: Install node_exporter
      hosts: nodes
      roles:
         - node_exporter_role

License
-------

BSD

Author Information
------------------

Emil Temerbulatov

