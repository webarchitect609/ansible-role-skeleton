Skeleton for Ansible role
=========================

Requirements
------------

- [Ansible](https://www.ansible.com/)
- `bash`, if you plan to use `bin/init`

How to use
----------

### Init script

1. Clone this repo
2. Make a symlink inside `~/bin`(which must be in `$PATH`), pointing to `bin/init` in this repo. For example:
   ```shell
   ln -s ~/projects/webarchitect609/ansible-role-skeleton/bin/init ~/bin/my-ansible-galaxy-role-init
   ```
3. Now go to any dir and call `init` script from there
   ```shell
   ~/projects/webarchitect609/ansible-role-skeleton/bin/init baz
   ```
   or just
   ```shell
   my-ansible-galaxy-role-init baz
   ```
   and the folder `ansible-role-baz` will be created, tuned for developing `webarchitect609.baz` Ansible role.

### General usage

```shell
ansible-galaxy role init --offline --role-skeleton "$SKELETON_DIR" -- "$ROLE_NAME"
```

, where `$SKELETON_DIR` is the dir where current repo is cloned and `$ROLE_NAME` is the name of the role, but without
vendor.

Then you have to go in role dir and manually remove `.idea` & `bin` directories.
