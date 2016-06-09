Role Name
=========

Chef Client installtion from the client side.

Requirements
------------

The validation.pem is expected to be on the ansible server alone. I don't feel comfortable putting a private key on a public repo. Even if encrypted.
You should use this with access to the internet so it can download the RPM if you don't have private repos. if you do, and they are configured to the boxes then change the variables to reflect that. This has been developed on EL7 platform with ansible 2.1.

Role Variables
--------------

A description of the settable variables for this role should go here, including any variables that are in defaults/main.yml, vars/main.yml, and any variables that can/should be set via parameters to the role. Any variables that are read from other roles and/or the global scope (ie. hostvars, group vars, etc.) should be mentioned here as well.

* chef_url_package: https://packages.chef.io/stable/el/7/chef-12.10.24-1.el7.x86_64.rpm  This variable is the chef package variable, it is responsible for the installation of the right package on your system. I would normally expect organization repositories to be managed and only the name of the package to be mentioned here
* chef_server_hostname: chef-server.example.com the chef server
* chef_server_ssl_port: 443 the expected communication port
* chef_server_url: "https://{{ chef_server_hostname }}/organizations/" what the default URL should look like
* chef_organization: poc - the name of the organization
* chef_environment: test - the name of the environment you want he client to be part of 
* chef_config_dir: '/etc/chef/' - the default configuration repository
* chef_roles: base - the default named policy role (chef-client -n <name>)


Dependencies
------------

A list of other roles hosted on Galaxy should go here, plus any details in regards to parameters that may need to be set for other roles, or variables that are used from other roles.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

```
    - hosts: all
      become: yes
      become_method: sudo
      roles:
        - chef-enrollment      
```
License
-------

BSD

Author Information
------------------

An optional section for the role authors to include contact information, or a website (HTML is not allowed).
