nextpertise.supervisord
==============================

Supervisord role for Debian hosts

Install it with the following command:

```bash
$ ansible-galaxy install nextpertise.supervisord
```

Requirements
------------

None

Role Variables
--------------

You can find a list of all available variables in ``defaults/main.yml``

Dependencies
------------

None

Example Playbook
-------------------------

    - hosts: servers
      roles:
         - role: nextpertise.supervisord
           supervisord_program:
             - name: django-uwsgi
               # directory to cwd to before exec (def no cwd)
               directory: "{{ project_home_path }}"
               command: "program_to_execute.sh"
               autostart: "true"
               autorestart: "true"
               stdout_logfile: "syslog"
               stderr_logfile: "syslog"

License
-------

GNUv2

Author Information
------------------

Teun Ouwehand @ Nextpertise B.V. (https://www.nextpertise.nl)
