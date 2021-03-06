Looking Glass
============

[![Gitter](https://badges.gitter.im/Join%20Chat.svg)](https://gitter.im/getglass/looking-glass?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)

Looking Glass is a set of technologies to create, manage and maintain a company's networks and services. 

Core technologies
-----------------
* Ansible
* LizardFS

Goals
-----
* (Almost) zero touch service deployment
* Builds highly available services
* Builds horizontally scalable services

Getting Started
===============
Requirements
------------
For a single machine and orchestrator:
* Ubuntu 12.04/14.04 or Debian 7 host machine
* Ansible 1.7+ installed
* sshpass installed

For multiple machines and a single orchestrator:
* Ubuntu 12.04/14.04 or Debian 7 host machine
* Ansible 1.7+ installed
* sshpass installed
* Client machines running Ubuntu 12.04/14.04, Debian 7 or CentOS 6+

Usage
-----
First-time usage:
* Install Ansible 1.7+ and sshpass on your management workstation
* Clone the Looking Glass repositories.

`git clone https://github.com/getglass/looking-glass.git`

`git clone https://github.com/getglass/looking-glass-secrets.git`

* Follow the instructions for the looking-glass-secrets repository
* To create the "glass" user according to your preferences (set in group_vars/all), run Looking Glass in "bootstrap" mode.

`ansible-playbook site.yml -i inventory --ask-pass --ask-sudo-pass`

* For future runs, simply use this command.

`ansible-playbook site.yml -i inventory` 

* You can also add "--limit=hostgroup" to limit your runs to a specific set of hosts.

Contact Us
==========

IRC
---
You can find us on IRC at #lookingglass on irc.freenode.net. The IRC channel is a good place to get help or discuss development of Looking Glass. However, as Looking Glass is not currently in wide distribution, the Gitter channel at the top of this README will be more helpful to you.

Project Details
===============

License
-------
looking-glass and looking-glass-secrets are made available under the MIT license. See the [LICENSE](LICENSE) file for details.

Branch Info
-----------
* Releases are named after Cloud Cult songs.
* The 'master' branch corresponds to the release actively under development.
* vX.Y.Z tags exist for previous releases.

TODO
----
This is a TODO list specific to the overall project (for tasks that do not belong in a particular module).
* Create a playbook to automatically pull down the latest Ansible on Ubuntu/CentOS?
