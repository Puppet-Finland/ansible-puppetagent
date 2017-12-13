# ansible-puppetagent

Ansible role for installing Puppet from Puppetlabs and optionally configuring
and running Puppet Agent.

# Usage

This role has the following parameters:

* *puppetagent_server*: puppetserver name. Defaults to 'puppet'. Example: 'puppet.domain.com'
* *puppetagent_manage_agent*: whether to configure and run the agent. Valid values are true and false (default)
* *puppetagent_waitforcert*: wait for the puppetserver to sign the certificate request. Valid values are true (default) and false.
