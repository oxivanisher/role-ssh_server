ssh_server
==========

Install and configure the openssh server.

Requirements
------------

None

Note
----
The you have to specify the `no` and `yes` options as strings (i.e. like `"no"` and `"yes"`), or Ansible will write them as boleans (`true` and `false`).

Role Variables
--------------

| Name                       | Comment                                                                   | Default value |
|----------------------------|---------------------------------------------------------------------------|---------------|
| ssh_server_set_options     | Set SSHD options to "key value"                          |                | `[PermitRootLogin: without-password, DebianBanner: "no", X11UseLocalhost: "no"]` |
| ssh_server_comment_options | The directory in the os users home where the cloud will be mounted        | `[Banner]`    |
| ssh_server_remove_options  | Your Nextcloud webdav URL (i.e. https://your.cloud.tld/remote.php/webdav) | `[ KeyRegenerationInterval, ServerKeyBits, RSAAuthentication, RhostsRSAAuthentication, UsePrivilegeSeparation]` |


Dependencies
------------

None

Example Playbook
----------------
```yaml
- name: Configure SSH Server
  hosts: server
  roles:
    - role: oxivanisher.linux_base.ssh_server
```

License
-------

BSD

Author Information
------------------

This role is part of the [oxivanisher.linux_base](https://galaxy.ansible.com/ui/repo/published/oxivanisher/linux_base/) collection, and the source for that is located on [github](https://github.com/oxivanisher/collection-linux_base).
