# project-2-ssh-tomcat-webapp

Instance --> ansible + jenkins = 1 instance
         --> tomcat = 1 instance
do all configuration in ansible and tomcat same
more configuration on jenkins need

--- #my playbook for project 2
- hosts: all
  become: true
  tasks:
  - name: copy war file to tomcat server
      copy:
        src: /home/ansible/project-2-ssh-tomcat-webapp.war  # file name should be same as artifactId & finalname
        dest: /root/apache-tomcat-9.0.76/webapps #tomcat version check
