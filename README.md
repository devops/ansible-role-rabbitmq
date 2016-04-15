# Role Name: RabbitMQ

An Ansible Role that installs RabbitMQ on RedHat/CentOS.

## Requirements

None.

## Role Variables

### `defaults/main.yml`

* `rabbitmq_cluster: Flase`
* `rabbitmq_erlang_cookie: OMZWYPRFPJDAUGKDSXAP`
* `rabbitmq_cluster_master: localhost`
* `rabbitmq_users:`
    ```
      - user: admin
        password: admin
        vhost: /
        configure_priv: .*
        read_priv: .*
        write_priv: .*
    ```

* `rabbitmq_users_removed:`
    ```
      - guest
    ```

## Dependencies

None.

## Example Playbook

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
        - role: rabbitmq
          rabbitmq_cluster: True
          rabbitmq_cluster_master: controller01
          rabbitmq_users:
            - user: openstack
              password: openstack
              vhost: /
              configure_priv: .*
              read_priv: .*
              write_priv: .*

## Author Information

z.
