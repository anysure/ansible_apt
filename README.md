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
| apt_aditional_packages | *none* | *list* | List of aditional packages to install on your system.  | 
| apt_aditional_repositories | *none* | *list* | List of repositories to add. |
| apt_autoclean | true | true/false | true to autoclean apt-get/aptitude cache (remove outdated downloaded deb files). |
| apt_autoremove | true | true/false | true to automatically uninstall unneeded dependencies installed by removed packages. | 
| apt_base_packages | a base list | *list* | List of basic packages to install on your system.  | 
| apt_base_repositories | a base repo list | *list* | List of repositories to add. WARNING! Removes everything else. Add ALL your repos before using it! Defaults to the default repos of Debian and Ubuntu based on your distribution and its version. |
| apt_force_apt_get | true | true/false | true to use apt-get / aptitude for package management.| 
| apt_install_recommends | true | true/false | false to disable recommended packages install. |
| apt_install_suggests | true | true/false | false to disable suggested packages install. |
| apt_required_packages | a base list | *list* | List of repositories to add. |
| apt_unattended_upgrade_origins_patterns | *none* | *list* | List of repositories to add. |
| apt_unattended_upgrade_package_blacklist | *none* | *list* | List of repositories to add. |
| apt_unattended_upgrades_packages | *none* | *list* | List of repositories to add. |
| apt_update_cache | true | true/false | false to update apt cache before installing/upgrading. |
| apt_upgrade | true | true/false | true to upgrade your system automatically. | apt_periodic_update_package_lists | *none* | *list* | List of repositories to add. |
| apt_templates_dest_path | | | 
| apt_templates_src_path | | |
| apt_periodic_download_upgradeable_packages | | |
| apt_periodic_autoclean_interval | | |
| apt_periodic_unattended_upgrade | | |
| apt_unattended_upgrade_auto_fix_interrupted_dpkg | false | |
| apt_unattended_upgrade_minimal_steps | true | |
| apt_unattended_upgrade_install_on_shutdown | false | |
| apt_unattended_upgrade_mail | | |
| apt_unattended_upgrade_mail_only_on_error | false | |
| apt_unattended_upgrade_remove_unused_kernel_packages | true | |
| apt_unattended_upgrade_remove_unused_dependencies | true | |
| apt_unattended_upgrade_automatic_reboot | true | |
| apt_unattended_upgrade_automatic_reboot_with_users | false | |
| apt_unattended_upgrade_automatic_reboot_time | now | |
| apt_unattended_upgrade_syslog_enable | false | |
| apt_unattended_upgrade_syslog_facility | daemon | |


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
