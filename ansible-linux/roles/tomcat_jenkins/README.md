Role Name
=========

Installing Jenkins on Tomcat 

Requirements
------------

Variables defined in playbook bellow should be added in a vault file

Role Variables
--------------

Variables can be find in defaults and var files    

Dependencies
------------

Tested on a RHEL79 OS    
   
Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:
```
---
- name: Run Jenkins as servlet in Tomcat    
  hosts: target_host     
  become: true    
  vars:    
    tomcat_ver: 9.0.45     
    ui_manager_user: manager                    # User who can access the UI manager section only      
    ui_manager_pass: Zaq!2wsxCde34rfv      # UI manager user password     
    ui_admin_username: admin                    # User who can access bpth manager and admin UI sections     
    ui_admin_pass: Zaq!2wsxCde34rfv          # UI admin password      
    jenkins_user: jenadm    
    jenkins_pass: Zaq!2wsxCde34rfv    
    jenkins_fullname: Jenkins Admin     
    jenkins_email: jenadm@rhel79     

  roles:        
    - tomcat_jenkins            
...
```
License
-------

BSD

Author Information
------------------

An optional section for the role authors to include contact information, or a website (HTML is not allowed).
