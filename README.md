Ansible httpd role
=========

This role deploys an httpd application, by installing httpd and running it as a service. 

Next to that it deploys a default Apache webserver will be listening on a specified port.

To access the webserver this role also installs firewalld and runs it a service. Also it configures the firewall so that the webserver will be accessible on the specified port.


Requirements
------------

This role has no requirements on which it is built

Example Playbook
----------------
In the playbook you can specify the httpd version.

    - hosts: webserver

      roles:
      - role: "ansible-httpd-app"
        vars:
          httpd_version: 2.4.6

Role Variables
--------------


    
    ---
    # defaults file for myapache

    #document root directory
    ap_http_host_dir: "my_host_dir"

    #httpd configuration file name
    ap_http_conf_file: "my_host_dir.conf"

    #httpd port on which the webserver will be accessed
    ap_http_port: 8000

    #source code location
    ap_source_code_location: "files/source_code"


