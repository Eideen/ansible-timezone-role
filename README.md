ansible-timezone-role
=========

Role sets timezone, and sets and remove systemd ntp and FallbackNTP.

Requirements
------------

A system that uses systemd-timesync deamon.

Role Variables
--------------

* NTP: sets primary NTP servers.
* FallbackNTP:  Sets Fallback NTP server, used when all there is no DHCP NTP or main NTP severs available.
* timezone: Sets timezone. Available variables can be found her: https://wikipedia.org/wiki/List_of_tz_database_time_zones

For "FallbackNTP" and "NTP", if not defined, they will be removed.

Dependencies
------------

No dependencies of other roles.

Example Playbook
----------------

````yaml
    - hosts: all
      roles:
         - ansible-timezone-role
      vars:
        timezone: Europe/Oslo
        NTP: 192.168.0.1 192.168.0.2
        FallbackNTP: 0.pool.ntp.org 1.pool.ntp.org
````

License
-------

BSD

Author Information
------------------

https://github.com/Eideen/
