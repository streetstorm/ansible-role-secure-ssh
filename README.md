ansible-role-secure-ssh
=========

Role Variables
--------------

Option | Description
--- | ---
`secure_sshd_name` | Name of ssh daemon, default is `ssh`.
`secure_sshd_config` | Path to ssh daemon config, default is `/etc/ssh/sshd_config`.
`secure_ssh_user_groups` | List groups. Default is `sudo`.
`secure_ssh_nopasswd` | Create nopasswd config. Default is `true`.
`secure_ssh_identity_key` | Path to your identity key. Added to `~/.ssh/authorized_keys` on remote host if both `secure_ssh_identity_key` and `secure_ssh_user` are defined. Default is `undefined`.
`secure_ssh_user` | Username on remote host whose authorized keys will be modified. Uses only if `secure_ssh_identity_key` is defined. Default is `undefined`.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables
passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
        - { role: ansible-role-secure-ssh, secure_ssh_user: superuser, secure_ssh_identity_key: /home/superuser/.ssh/id_rsa.pub }

License
-------

BSD

Author Information
------------------

@streetstorm
