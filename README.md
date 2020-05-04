# Jenkins and Tomcat on CentOS 7 
These roles works butter smooth with the VM instances of GCP. I cloned the git repo of the ELK on my GCP VM and then ran runsetup.yaml. For GCP instances you need to install git/ansible.

* Install Jenkins 
* Install Tomcat 

Playbook - runsetup.yaml is fired on the localhost where jenkins is going to run.
```
# yum install ansible git 
# ansible-playbook runsetup.yaml -i elk_hosts
```
Please note: Jenkins is going to run on port 9090 as tomcat is also installed on same system which will run on port 8080. 
