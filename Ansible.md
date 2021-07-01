# OVERVIEW OF ANSIBLE AS A CONFIGURATION MANAGEMENT TOOL
Ansible is an automation engine that automates cloud provisioning, intra-service orchestration, application deployment and configuration management through YAML in the form of Ansible Playbooks. Configuration or Installation or deployment are done in a single YAML file and the same file can be used multiple times for different environments. 

Ansible connects your nodes and pushes out Ansible modules to them which are resource models of the desired state of the system. The modules are removed by Ansible after execution, over SSH by default. Each module handles a specific task.

Ansible Playbooks Orchestrate the module execution. Sequential modules are grouped in tasks where each task makes sure the module gets executed using arguments and a description of the task. Tasks being defined in a block is called a Play and there can be multiple plays in a single YAML file hence Playbook. 

Ansible has hosts file that keeps an inventory containing all the machines involved in task executions. Multiple IP addresses or host names can be grouped on the file. 

## ANSIBLE VS TERRAFORM
Terraform focuses on infrastructure automation where elements of desired environment are individually described along with their relationships to each other.evaluates the model, develops a plan based on the dependencies, and commands the IaaS in an optimal way.  It’s also idempotent and resource aware, meaning that repeated runs will do nothing if nothing in the environment or plan has changed.  If something has changed, it will synchronize the cloud infrastructure with the intent of the plan

With Ansible, Users create “playbooks” which are evaluated from top to bottom, and executed in sequence.  Playbooks typically concern themselves with the configuration of individual hosts or network devices, which lends itself to a procedural approach.  Ansible does have the ability to provision cloud infrastructure as well, but its procedural nature makes it ill suited to large infrastructure deployments.  Since Ansible is suited for configuration management, it isn’t really limited to cloud applications.  Ansible is as happy configuring bare metal servers as virtual ones.