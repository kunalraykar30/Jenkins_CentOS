# Jenkins and Tomcat on CentOS 7 
2 roles are written down which works butter smooth with the VM instances of GCP. I cloned the git repo of the ELK on my GCP VM and then ran runsetup.yaml. For GCP instances you need to install git/ansible.

* Install Jenkins - jenkins_role
* Install Tomcat - task is added inside jenkins_role

Playbook - runsetup.yaml is fired on the localhost where jenkins is going to run.
```
# yum install ansible git 
# ansible-playbook runsetup.yaml -i elk_hosts
```
User name - jenkins-deployer is added inside in tomcat so jenkins can deploy the war/ear file on tomcat. 

#### Please note: Jenkins is going to run on port 9090 as tomcat is also installed on same system which will run on port 8080. 
