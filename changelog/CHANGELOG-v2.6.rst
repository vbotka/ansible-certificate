====================================
vbotka.certificate 2.6 Release Notes
====================================

.. contents:: Topics


2.6.4
=====

Release Summary
---------------
Maintenance and feature update.

Major Changes
-------------
* Add var certificate_data_simple
* Add vars/simple.yml.sample
* Update vars.yml

Minor Changes
-------------
* Update README
* Split defaults/main.yml to defaults/main/*
* Remove all 'not ansible_check_mode'. All modules aupport check_mode
* Add var certificate_role_version
* Update debug.yml
* Comment vars/defaults/FreeBSD.yml

Bugfixes
--------

Breaking Changes / Porting Guide
--------------------------------


2.6.5
=====

Release Summary
---------------
Bugfix update.

Major Changes
-------------

Minor Changes
-------------

Bugfixes
--------
* Default certificate_acme_dir_mode_public="0755"

Breaking Changes / Porting Guide
--------------------------------


2.6.4
=====

Release Summary
---------------
Maintenance and feature update.

Major Changes
-------------
* Add var certificate_data_simple
* Add vars/simple.yml.sample
* Update vars.yml

Minor Changes
-------------
* Update README
* Split defaults/main.yml to defaults/main/*
* Remove all 'not ansible_check_mode'. All modules aupport check_mode
* Add var certificate_role_version
* Update debug.yml


2.6.3
=====

Release Summary
---------------
Sync var certificate_role_version


2.6.2
=====

Release Summary
---------------
Ansible 2.17 update

Major Changes
-------------
* Add support of FreeBSD 14.1, Ubuntu Noble

Minor Changes
-------------
* Add variable freebsd_install_state default=present
* Update README
* Update lint config
* Fix lint

Breaking Changes / Porting Guide
--------------------------------
* al_include_os_vars_path changed to incremental
  al_include_os_vars_path_incr. Updated vars/defaults


2.6.0
=====

Release Summary
---------------
Ansible 2.16 update

Bugfixes
--------

Breaking Changes / Porting Guide
--------------------------------
