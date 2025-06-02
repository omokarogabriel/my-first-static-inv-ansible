Role Name
=========
**webserver**
A brief description of the role goes here.
*This role help in installing apache2 server and enabling it start on boot*
Requirements
------------

Any pre-requisites that may not be covered by Ansible itself or the role should be mentioned here. For instance, if the role uses the EC2 module, it may be a good idea to mention in this section that the boto package is required.

Role Variables
--------------
*apache_service_name: apache2*
*apache_service:*
  - name: "{{ apache_service_name }}"
  - state: started
  - enabled: true  


A description of the settable variables for this role should go here, including any variables that are in defaults/main.yml, vars/main.yml, and any variables that can/should be set via parameters to the role. Any variables that are read from other roles and/or the global scope (ie. hostvars, group vars, etc.) should be mentioned here as well.

Dependencies
------------
*git-repo*
A list of other roles hosted on Galaxy should go here, plus any details in regards to parameters that may need to be set for other roles, or variables that are used from other roles.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

- name: Apply webserver role on webservers and deploy git repository
  hosts: webservers
  become: yes
  roles:
    - webserver
    - git-repo

License
-------

BSD

Author Information
------------------
***Gabriel Chukwuemeka Omokaro***
**An aspirng Cloud devOps Engineer**

An optional section for the role authors to include contact information, or a website (HTML is not allowed).
[github](https://github.com/omokarogabriel)