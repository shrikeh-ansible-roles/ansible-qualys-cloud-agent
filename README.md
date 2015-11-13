# Qualys Cloud Agent
=========
[![Ansible Role](https://img.shields.io/ansible/role/5948.svg)](https://galaxy.ansible.com/detail#/role/5948)
[![Build Status](https://travis-ci.org/shrikeh/ansible-qualys-cloud-agent.svg)](https://travis-ci.org/shrikeh/ansible-qualys-cloud-agent)
[![GitHub Stars](https://img.shields.io/github/stars/shrikeh/ansible-qualys-cloud-agent.svg)](https://github.com/shrikeh/ansible-qualys-cloud-agent)

This role installs the [Qualys Cloud Agent][qualys_cloud_agent] on Linux hosts. This is not yet production, or even testing, ready.

## Requirements
------------

Any pre-requisites that may not be covered by Ansible itself or the role should be mentioned here. For instance, if the role uses the EC2 module, it may be a good idea to mention in this section that the boto package is required.

## Role Variables
--------------

#### [`qualys_agent_pkg_state_latest`][qualys_agent_pkg_state_latest]
Default: `no`
Controls whether to use 'present' or 'latest' for package installation

#### [`qualys_agent_repository_uri`][qualys_agent_repository_uri]
Default: `wibble`
The repository to use for installation of the agent.

#### [`qualys_agent_activation_key`][qualys_agent_activation_key]
Default: None
Mandatory. The activation key for the asset to use for installation.

## Dependencies
------------

None.

## Example Playbook
----------------
```YAML
    - hosts: servers
      vars:
        qualys_agent_activation_key: "{{ lookup('env', 'TEST_QUALYS_AGENT_ACTIVATION_KEY') }}"
      roles:
         - { role: shrikeh.qualys-cloud-agent }
```

 ## License
 -------

 [MIT][licence]

Author Information
------------------

An optional section for the role authors to include contact information, or a website (HTML is not allowed).

[qualys_cloud_agent]: https://www.qualys.com/enterprises/security-compliance-cloud-platform/
[qualys_agent_pkg_state_latest]: https://github.com/shrikeh/ansible-qualys-cloud-agent/blob/master/defaults/main.yml#L3
[qualys_agent_repository_uri]: https://github.com/shrikeh/ansible-qualys-cloud-agent/blob/master/defaults/main.yml#L4
[licence]: https://raw.githubusercontent.com/shrikeh/ansible-qualys-cloud-agent/master/LICENSE
