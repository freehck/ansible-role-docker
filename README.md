docker
=========

Role docker installs docker.io package ans allow to set your own private insecure registry for a user

Description
--------------

This role is for local insecure registries only. Use it only on LOCAL NETWORK.

Role Variables
--------------

 - set_registry: default no
 - registry: url of your private registry
 - config_user: user to configure not to auth with this registry

Example 1 (short)
----------------

    - hosts: k8s-cluster
      become: yes
      become_user: root
      roles:
        - role: docker
          set_registry: yes
          registry: registry.crptech.local:80
          tags: [master, slave, docker]

License
-------

GPLv3+

Author Information
------------------

This role was written by Dmitrii Kashin aka freehck
