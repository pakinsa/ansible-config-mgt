# ansible-config-mgt
A test project with Ansible

Purpose: Automate the configuration of 2 Webservers, 1 DB Server, 1 NFS server, and 1 LB server using Ansible and Jenkins


### Required Steps:



1. Set up a webhook link from your source code repository (such as GitHub, Jira, or Trello) to trigger a Jenkins job whenever there is a change in the code. This will allow to automate the deployment of your code to the managed nodes using Jenkins. This will help you to keep track of the history and status of your deployments.

    a. Create a new repo named ansible-config-mgt
    
    b. Create an EC2 server named "Jenkins-Ansible" and Install and configure with ansible and Jenkins, and use Elastic IP addressing to avoid change in IPs when you shut down the instance

    c. Create a freestyle project named "ansible" on Jenkins

    d. Create a webhook link from the GitHub repo to the "Jenkins-ansible" server

    e. Allow and test Automatic job build to the "Jenkins-ansible" server on the main branch from your repo.


