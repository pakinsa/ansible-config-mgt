# ansible-config-mgt
A test project with Ansible and details about Jenkins

Purpose: Automate the configuration of 2 Webservers, 1 DB Server, 1 NFS server, and 1 LB server using Ansible and Jenkins


### Required Steps:



1. Set up a webhook link from your source code repository (such as GitHub, Jira, or Trello) to trigger a Jenkins job whenever there is a change in the code. This will allow you to automate the deployment of your code to the managed nodes using Jenkins. This will help you to keep track of the history and status of your deployments.

    a. Create a new repo named ansible-config-mgt
    
    b. Create an EC2 server named "Jenkins-Ansible" and Install and configure with ansible and Jenkins, and use Elastic IP addressing to avoid change in IPs when you shut down the instance

    c. Create a freestyle project named "ansible" on Jenkins

    d. Create a webhook link from the GitHub repo to the "Jenkins-ansible" server

    e. Allow and test Automatic job build to the "Jenkins-ansible" server on the main branch from your repo.


### Jenkins is highly extensible and customizable, thanks to its plugin architecture. There are hundreds of plugins available for Jenkins that can enhance its functionality and integrate with various tools and services. Some of the most popular plugins are:

#### Git: This plugin allows Jenkins to integrate with Git, one of the most widely used version control systems. It enables Jenkins to clone, fetch, and checkout Git repositories, and trigger builds based on Git events, such as commits, branches, tags, etc.

#### Pipeline: This plugin allows Jenkins to implement and execute a project as a pipeline, which is a sequence of stages that perform different tasks, such as building, testing, deploying, etc. A pipeline can be defined using a domain-specific language (DSL) called Groovy, or using a graphical editor called Blue Ocean. A pipeline can also be stored as a file called Jenkinsfile in the source code repository, which enables versioning and collaboration of the pipeline definition.

#### Maven: This plugin allows Jenkins to integrate with Maven, one of the most popular build automation tools for Java projects. It enables Jenkins to invoke Maven goals and phases, and use Maven settings and profiles. It also provides support for Maven reports, such as test results, code coverage, code quality, etc.

#### JUnit: This plugin allows Jenkins to integrate with JUnit, one of the most popular testing frameworks for Java projects. It enables Jenkins to parse and display JUnit test results, and mark builds as unstable or failed based on the test outcome. It also provides support for test trends, test history, and test flakiness analysis.

2. The /var directory in Jenkins is neither a root nor a home folder, but a subdirectory of the Jenkins installation directory. It contains various files and folders that are used by Jenkins, such as logs, plugins, jobs, etc. The /var directory has a parent folder, which is the Jenkins installation directory, which can vary depending on how Jenkins was installed and configured. For example, if Jenkins was installed using the Debian package, the installation directory would be /usr/share/jenkins, and the /var directory would be /usr/share/jenkins/var. If Jenkins was installed using the WAR file, the installation directory would be the location of the WAR file, and the /var directory would be a subdirectory of that location.

3. Ansible is a robust configuration management and interesting content

Ansible using yum. It seems that the Ansible package is not available in the default repositories of your system. You may need to enable the Extra Packages for Enterprise Linux (EPEL) repository first, which contains the Ansible package and many other useful packages. To enable the EPEL repository, you can run


According to the web search results I found, the latest version of Ansible depends on whether you are referring to the Ansible community package or ansible-core. The Ansible community package is a collection of modules, plugins, and roles that offer the functionality that existed in Ansible 2.9, while ansible-core is the minimal set of modules and plugins required to run Ansible. The Ansible community package uses a new versioning system that follows semantic versioning rules, while ansible-core continues the “classic Ansible” versioning1.

As of November 2021, the latest version of the Ansible community package is 4.8.0, which was released on November 9, 2021. This version is based on ansible-core 2.11.7, which was released on November 2, 20212. You can install the Ansible community package using the pip command, such as:

$ pip install ansible

The latest version of ansible-core is 2.12.0, which was released on November 16, 2021. This version introduces many new features and improvements, such as the ansible-test command, the ansible-galaxy collection init command, the ansible-inventory --graph --yaml option, and more3. You can install ansible-core using the pip command, such as:

$ pip install ansible-core
   


You can create the /etc/ansible directory in Linux Ubuntu if it does not exist already. This directory is the default location for Ansible configuration and inventory files on most Linux systems. To create this directory, you need to use the mkdir command in the terminal. The mkdir command stands for make directory and it allows you to create new directories in the file system. To use the mkdir command, you need to type mkdir followed by a space and the name of the directory you want to create. For example, to create the /etc/ansible directory, you would type:

$ sudo mkdir /etc/ansible

and then press [Enter]. You may need to enter your password to confirm the command. This will create the /etc/ansible directory in the /etc directory. You can verify this by using the ls command, which stands for list and it shows you the files and directories in your current location. For example, after creating the /etc/ansible directory, you would see something like this:


Permission to Copy Artifact in Jenkins means that you can copy the files or folders that are generated or stored by another Jenkins job. For example, you may want to copy the binary files, test results, or configuration files from one job to another. This can help you reuse the artifacts and avoid duplicating the work.

To copy the artifacts from another job, you need to use the Copy Artifact Plugin ¹, which provides a build step and a pipeline step that allow you to specify the source job, the files to copy, and the destination directory. You can also use variables, filters, and parameters to customize the copy operation.

However, not every job can copy the artifacts from another job. You need to have the permission to do so. To grant permission to copy artifacts in Jenkins, you need to enable authorization and grant permission 'Copy Artifact' to the project. In the project configuration, go to General -> Permission to Copy Artifact, check the box and set the projects that can copy the artifact. Alternatively, you can add information about which task can copy artifacts on the job setup page. The Copyartifact plugin treats builds running as an anonymous, so copying artifacts is allowed if the project with artifacts is readable from anonymous ².

I hope this helps you understand what Permission to Copy Artifact in Jenkins means. Let me know if you have any other questions! 😊

Source: Conversation with Bing, 01/12/2023
(1) Jenkins CopyArtifact step - Unable to find project for artifact copy. https://stackoverflow.com/questions/48834762/jenkins-copyartifact-step-unable-to-find-project-for-artifact-copy.
(2) . https://bing.com/search?q=Permission+to+Copy+Artifact+in+jenkins+means.
(3) Jenkins Permission to Copy Artifact is always granted. https://stackoverflow.com/questions/49425700/jenkins-permission-to-copy-artifact-is-always-granted.
(4) jenkins - Grant copy artIfact permission in multi-branch pipeline .... https://stackoverflow.com/questions/47771722/grant-copy-artifact-permission-in-multi-branch-pipeline.
(5) How to add permission to copy artifacts in Jenkins - Czerniga. https://www.czerniga.it/2022/01/05/how-to-add-permission-to-copy-artifacts-in-jenkins/.
(6) Copy Artifact | Jenkins plugin. https://plugins.jenkins.io/copyartifact/.
(7) undefined. https://wiki.jenkins.io/JENKINS/Copy-Artifact-Plugin.html.
(8) undefined. https://wiki.jenkins.io/display/JENKINS/Copy+Artifact+Plugin.


I’m sorry, you are getting this error because you have specified an invalid path for the ansible-config-artifact file. The file does not exist in the /home/ubuntu directory, and Ansible cannot find or access it. This file is supposed to contain the configuration settings for Ansible, such as the inventory file, the roles path, the remote user, etc. If you do not have this file, Ansible will use the default settings, which may not suit your needs.

To fix this error, you need to create the ansible-config-artifact file in the /home/ubuntu directory, or in another location that you can specify with the ANSIBLE_CONFIG environment variable. You can use the ansible-config command to generate a template for this file, or you can refer to the official documentation 1 or the tutorials on DigitalOcean 2 or DevOpsCube 3 for more information on how to create and customize the Ansible configuration file.

I hope this helps you resolve the error and use Ansible properly. Let me know if you have any other questions! 😊