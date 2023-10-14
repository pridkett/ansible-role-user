ansible-role-user
=================

Patrick Wagstrom &lt;160672+pridkett@users.noreply.github.com&gt;

October 2023

Overview
--------

This is a really simple ansible role that I created just to ensure that I had the correct username and SSH keys on any new server I create.

Configuration
-------------

The following variables are available for configuration:

- `username`: The name of the user to create. No default.
- `ssh_public_key`: The public key for the new user.
- `ssh_private_key`: The private key for the new user. This really should be stored in `secrets.yml`.
- `authorized_keys`: A list of public keys that should be added to the `~/.ssh/authorized_keys` file for the user.

It expects some of the variables to be saved in the secrets file `secrets.yml`

None of these variables have default values.

Example Playbook
----------------

```yaml
- hosts:
    - raspberrypi4-office.wagstrom.net
  roles:
    - pridkett.user
  vars:
    username: pwagstro
```
		 
License
-------

MIT
