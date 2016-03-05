Role Name
========

This Ansible role lets you install Zend Server on the specified host

Requirements
------------

Nothing, it runs out of the box.

Role Variables
--------------

In the current version, you can specify the following variables:

| Name                         | Default |                                                    |
|------------------------------|---------|----------------------------------------------------|
| zendserver_version           | 6.3     | The version of Zend Server to install              |
| zendserver_community_edition | false   | Install Zend Server Community Edition. This is only relevant to Zend Server 5 and below. |
| zendserver_gui_password      |         | The password for the Zend Server GUI               |
| php_version                  | 5.5     | The version of PHP to install                      |
| php_cli_in_path              | true    | Add the Zend Server binary dir to the bash profile |


Dependencies
------------

This package has no dependencies on modules not included with Ansible by default.

License
-------

MIT

Author Information
------------------

Created by Richard Tuin
https://www.twitter.com/Richard_Tuin
http://www.rtuin.nl

Examples
--------

```
---
- name: Zend Server test
  hosts: all
  roles:
    - rtuin.zendserver
```

Or, using parameters:

```
---
- name: Zend Server test
  hosts: all
  roles:
    - { role: rtuin.zendserver, php_version: 5.4, zendserver_version: 6.2 }
```
