Role Name: bes_install
=========

Installation of BES client on Windows Server systems

Requirements
------------

Windows instances are part of CMS 1.x project, where BES Client is used for getting software and patches installed on.
Kerberos is configured on Ansible controller node to allow user authentication to the domain that VM belongs to.

Role Variables
--------------

Few variables are declared in vars/main.yml like:   
   `` src: C:\win_upgrade``       
   `` bes_src: '{{ src }}\BESclient' ``      
   `` ir_sds: 146.89.169.235``        
   `` sr_sds: 146.89.141.138``       
   `` drive: "{{ ansible_facts['env']['SystemDrive'] }}"``    


Dependencies
------------

    dependencies:
    - role: work_dir

Example Playbook
----------------

    - hosts: servers
      roles:
         - { role: bes_install, when: "ansible_facts['os_family'] == 'Windows'" }

License
-------

BSD

Author Information
------------------

Narcis Serbanescu (narcis.serbanescu@gmail.com)

