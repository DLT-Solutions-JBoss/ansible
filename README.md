## Fuse on EAP - JBoss Deployment

- Requires Ansible 2 or newer
- Expects RHEL 7.x hosts

<<<<<<< HEAD
These playbooks dllow you to 
- Deploy a EC2 server from scratch
- Deploy a very basic implementation of JBoss Enterprise Application Platform (EAP), version 6.4
- Deploy a Fuse server on top of the EAP instance

To use them, first edit the appropriate "hosts" inventory file to contain the hostnames of the machines on which you want JBoss software deployed, and edit the group_vars/jboss-servers file to set any JBoss configuration parameters you need.

Then run the playbook, like this:

	ansible-playbook -i <hosts file> <desired site>.yml --private-key-file <path and filename to key file for target servers>

When the playbook run completes, you should be able to see the JBoss EAP Server running on the ports you chose, on the target machines.

This is a very simple playbook and could serve as a starting point for more complex JBoss-based projects. 
=======
These playbooks deploy a very basic implementation of Red Hat's Fuse version 6.2.1 onto an instance of 
JBoss Enterprise Application Platform (EAP) version 6.4. 

To use them, first edit the "hosts" inventory file to contain the
hostnames of the machines on which you want JBoss deployed, and edit the 
group_vars/jboss-servers file to set any JBoss configuration parameters you need.

Then run the playbook, like this:

	ansible-playbook -i hosts fuse_on_eap-site.yml

When the playbook run completes, you should be able to see the JBoss
EAP server running on the ports you chose, on the target machines, 
and with the ability to deploy Fuse applications.

This is a very simple playbook and is intended to use as a starter kit to 
configure an application infrastructure for your needs. You can expand the (ansible/jboss-standalone/roles/fuse-eap-standalone/)
tasks to deploy testing servers, their scripts, to compliment your CI/CD pipelines.
>>>>>>> 2aac49153aac60f201f553250e96e6a24613f92e

### Ideas for Improvement

Here are some ideas for ways that these playbooks could be extended:

- Write a playbook or an Ansible module to configure JBoss users.
- Write a playbook to deploy an actual application into the server.
- Extend this configuration to configure load balancers or other web server frontends to enable/disable based on playbook task needs to conduct rolling updates into the playbook run.

<<<<<<< HEAD
We would love to see contributions and improvements, so please fork this repository on GitHub and send us your changes via pull requests.
=======
I would love to see contributions and improvements, so please fork this
repository on GitHub and send us your changes via pull requests.
>>>>>>> 2aac49153aac60f201f553250e96e6a24613f92e
