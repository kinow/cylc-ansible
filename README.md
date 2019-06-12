# The cylc-core Ansible Role

[![Build Status](https://travis-ci.org/alanbchristie/ansible-role-cylc-core.svg?branch=master)](https://travis-ci.org/alanbchristie/ansible-role-cylc-core)
[![GPLv3 license](https://img.shields.io/badge/License-GPLv3-blue.svg)](http://perso.crans.org/besson/LICENSE.html)

An [Ansible] Role for the installation of the [Cylc] workflow engine.

The **cylc-core** role installs cylc (into the `/opt` directory) and adjusts
the system-wide `PATH` environment variable so all users have access to it
by placing a file in `/etc/profile.d`. The term _core_  is used as this
Role is for a _headless_ server, i.e. one without graphical/display
capabilities - a Cylc engine to be configured and used from the command-line.

## Role variables
Available variables and default values (see [defaults/main.yml](defaults/main.yml)): -

    cylc_version: 7.8.2

## Example playbook

    ---
    - hosts: cylc-server
      tasks:
      - include_role:
          name: alanbchristie.cylc-core

---

[Ansible]: https://pypi.org/project/ansible/
[Cylc]: https://cylc.github.io
