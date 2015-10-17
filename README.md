ansible-role-ntpclient [![Build Status](https://travis-ci.org/okfine/ansible-role-ntpclient.svg?branch=master)](https://travis-ci.org/okfine/ansible-role-ntpclient)
=========

Ansible role to install and configure NTP client.

Requirements
------------

This role is designed for use on the Operating Systems listed below.

* RHEL/CentOS
* Debian/Ubuntu

Role Variables
--------------

The ```ntp_enable``` variable allows you to enable or disable the NTP service itself.  
Disabling the NTP service can be useful within certain virtual environments.

	ntp_enable: true

The ```ntp_servers``` variable allows for the definition of user-defined NTP servers.
By default, this role utilizes the main pools at [pool.ntp.org](http://www.pool.ntp.org/en/use.html).

	ntp_servers:
	  - 0.pool.ntp.org
	  - 1.pool.ntp.org
	  - 2.pool.ntp.org
	  - 3.pool.ntp.org

Dependencies
------------

None

Example Playbook
----------------

    - hosts: servers
      roles:
         - { role: ansible-role-ntpclient }

License
-------

BSD / MIT

Author Information
------------------

[okfine](https://github.com/okfine)
