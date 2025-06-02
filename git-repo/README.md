Role Name
=========
**git-repo**
A brief description of the role goes here.
*This role help in deploying a remote repo to the server using ansible*
Requirements
------------
- git must be installed
- when using a private repo, you will save the private key with *ssm* and create  a role for *ec2* to have acces to the ssm resource.
- add the policy to the role and create an instance profile, then attach the instance profile to the instance when creating


Any pre-requisites that may not be covered by Ansible itself or the role should be mentioned here. For instance, if the role uses the EC2 module, it may be a good idea to mention in this section that the boto package is required.

Role Variables
--------------
*my_git_repo: 'https://github.com/omokarogabriel/portfolio.git'*
*my_git_dest: '/var/www/html/portfolio'*
*my_git_version: 'main'*
*my_git_update: yes*
*my_git_force: yes*
A description of the settable variables for this role should go here, including any variables that are in defaults/main.yml, vars/main.yml, and any variables that can/should be set via parameters to the role. Any variables that are read from other roles and/or the global scope (ie. hostvars, group vars, etc.) should be mentioned here as well.

Dependencies
------------
- webserver(also a role created along side git-repo, apache2)

A list of other roles hosted on Galaxy should go here, plus any details in regards to parameters that may need to be set for other roles, or variables that are used from other roles.

Example Playbook
----------------
*site.yml*
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