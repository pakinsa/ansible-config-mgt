# ansible-config-mgt
A test project with Ansible and details about Jenkins

Purpose: Automate the configuration of 2 Webservers, 1 DB Server, 1 NFS server, and 1 LB server using Ansible and Jenkins


### Required Steps:



1. Set up a webhook link from your source code repository (such as GitHub, Jira, or Trello) to trigger a Jenkins job whenever there is a change in the code. This will allow to automate the deployment of your code to the managed nodes using Jenkins. This will help you to keep track of the history and status of your deployments.

    a. Create a new repo named ansible-config-mgt
    
    b. Create an EC2 server named "Jenkins-Ansible" and Install and configure with ansible and Jenkins, and use Elastic IP addressing to avoid change in IPs when you shut down the instance

    c. Create a freestyle project named "ansible" on Jenkins

    d. Create a webhook link from the GitHub repo to the "Jenkins-ansible" server

    e. Allow and test Automatic job build to the "Jenkins-ansible" server on the main branch from your repo.


2. Jenkins is a tech tool that saves artifacts.

3. Pipeline: This plugin allows Jenkins to implement and execute a project as a pipeline, which is a sequence of stages that perform different tasks, such as building, testing, deploying, etc. A pipeline can be defined using a domain-specific language (DSL) called Groovy, or using a graphical editor called Blue Ocean. A pipeline can also be stored as a file called Jenkinsfile in the source code repository, which enables versioning and collaboration of the pipeline definition.

4. Maven: This plugin allows Jenkins to integrate with Maven, one of the most popular build automation tools for Java projects. It enables Jenkins to invoke Maven goals and phases and use Maven settings and profiles. It also provides support for Maven reports, such as test results, code coverage, code quality, etc.

5. The /var directory in Jenkins is neither a root nor a home folder, but a subdirectory of the Jenkins installation directory. It contains various files and folders that are used by Jenkins, such as logs, plugins, jobs, etc. The /var directory has a parent folder, which is the Jenkins installation directory, which can vary depending on how Jenkins was installed and configured. For example, if Jenkins was installed using the Debian package, the installation directory would be /usr/share/jenkins, and the /var directory would be /usr/share/jenkins/var. If Jenkins was installed using the WAR file, the installation directory would be the location of the WAR file, and the /var directory would be a subdirectory of that location.
   


