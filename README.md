[![Build Status](https://img.shields.io/travis/quocvu/nodejs-ansible.svg)](https://travis-ci.org/quocvu/nodejs-ansible)
[![Ansible Role](https://img.shields.io/ansible/role/20548.svg)](https://galaxy.ansible.com/quocvu/openbox-archlinux)

openbox-archlinux
=================

Install and configure OpenBox window manager on ArchLinux.
Configure theme, wallpaper, menu, and optimize for best performance.

Requirements
------------

Ansible, internet connection, a user account on the host target.
Because this playbook puts files in the user home folder, it as advised to
use the same account as you would normally use with your desktop to run
with Ansible.

Ansible 2.4 is required to manipulate XML documents.  To install it:

    $ sudo CFLAGS=-Qunused-arguments CPPFLAGS=-Qunused-arguments pip install git+https://github.com/ansible/ansible.git@stable-2.4


Role Variables
--------------

* `launchers`: list of apps to put in the dock
* `dock_hide_mode`: If 0, the dock won't hide.  If 1, the dock intelligently hides.  If 2, the dock auto-hides. If 3, the dock dodges active maximized windows. If 4, the dock dodges every window.
* `dock_icon_size`: The size of dock icons (in pixels) in the dock
* `dock_position`: The position for the dock on the monitor.  If 0, left.  If 1, right.  If 2, top.  If 3, bottom.
* `dock_theme`: The name of the dock's theme to use
* `openbox_config`: key value pairs of OpenBox settings

Dependencies
------------

Needs Python

Example Playbook
----------------

To install Openbox windows manager, add the following in your playbook:

```
- hosts: servers
  roles:
    - { role: quocvu.openbox-archlinux }
```

License
-------

MIT

Author Information
------------------

Quoc Vu  

* https://linkedin.com/in/quocvu  
* https://github.com/quocvu
