Loki Ansible Role
=========

This Ansible role installs and configures Loki, a log aggregation system from **Grafana**. Logs can be viewed in **Grafana** and stored in multiple backends like **S3**, **GCS**, **Azure Blob Storage**, etc.

Requirements
------------

- [Ansible](https://www.ansible.com/) - Ansible must be installed to execute the playbook.
- [Docker](https://www.docker.com/) - Docker must be installed to run promtail as a container.
- [Promtail](https://grafana.com/docs/loki/latest/clients/promtail/) - Promtail must be installed to another server and accessible to Loki.

Role Variables
--------------

| Variable | Description | Default |
|----------|-------------|---------|
| `loki_config_file_path` | Path to the Loki configuration file | `files/loki-config.yaml` (on ansible **control node**) |

Dependencies
------------

None

Example Playbook
----------------

```yaml
- hosts: servers
  roles:
    - promtail
```

License
-------

BSD