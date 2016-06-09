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



Dependencies
------------

A list of other roles hosted on Galaxy should go here, plus any details in regards to parameters that may need to be set for other roles, or variables that are used from other roles.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: username.rolename, x: 42 }

License
-------

BSD

Author Information
------------------

An optional section for the role authors to include contact information, or a website (HTML is not allowed).
