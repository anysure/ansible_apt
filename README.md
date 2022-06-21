ansible_apt
===========

This is the AnySURE role ansible_apt. It configures the APT repositiry's on a Debian system. Installs and upgrades packages.

Requirements
------------

none

Role Variables
--------------

| Variable | default | options | description |
|----------|---------|---------|-------------|
| apt_install_recommends | yes | yes/no | no to disable recommended packages install. |
| apt_update_cache | yes | yes/no | no to update apt cache before installing/upgrading. |
| apt_force_apt_get | yes | yes/no| no to use apt-get / aptitude for package management.| 
| apt_upgrade | yes| yes/no | yes to upgrade your system automatically. |
| apt_autoclean | yes | yes/no | yes to autoclean apt-get/aptitude cache (remove outdated downloaded deb files). |
| apt_autoremove | yes| yes/no | yes to automatically uninstall unneeded dependencies installed by removed packages. | 
| apt_base_packages | a base list | *list* | List of basic packages to install on your system.  | 
| apt_aditional_packages | *none* | *list* | List of aditional packages to install on your system.  | 
| apt_base_repositories | a base repo list | *list* | List of repositories to add. WARNING! Removes everything else. Add ALL your repos before using it! Defaults to the default repos of Debian and Ubuntu based on your distribution and its version. |
| apt_aditional_repositories | *none* | *list* | List of repositories to add. |


Dependencies
------------

None.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - ansible_apt

License
-------

Apache 2.0

Author Information
------------------

Ronny Roethof <ronny.roethof@anylinq.com>
