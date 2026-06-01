# Summary

I'm slowly stepping foot into Linux Automation, it's part of becoming a great Linux Administrator, automation is very much involved with Linux to automate tedious tasks and list of commands. This repository will serve as my experience with Ansible journey from start to deep in-depth. 

# Setup

The first project I'm doing is a complicated one, at least for me is Kubernetes setup with Control Master and the Node Workers, I've made simple Ansible playbooks in the fast where just updates and installs simple packages like curl but nothing more comprehensive like a Kubernetes setup. Surely, I can find a great Ansible playbook that does this but this would default the purpose of my learning. 

# Project 01: Kubernetes Deployment 


<img width="318" height="156" alt="image" src="https://github.com/user-attachments/assets/e7f8eaf9-3e4e-499b-86c5-457c91ace29e" />

**Annotations:** 
- **Hosts:** Has all of the Servers that we need, for the sake of testing we only have two servers, the Master and Nodes 
- **Needed_files:** Is the files that we need, I figured it would be easier and safer if we over-write simple changes rather then having Ansible finding an exact line and changing it. Which includes the config.toml for the containerd and sysctl. 
- **Roles**: Has the master and the nodes configuration so we can have a clean Ansible playbook setup.
- **Kube_deploy_playbook**: Is the main playbook which uses very simple pre task and calls out the roles, the master and the nodes. 



<img width="496" height="438" alt="image" src="https://github.com/user-attachments/assets/e1576aa0-bf1c-44fb-881d-486f041aed24" />

**Annotations:** The pre_tasks simply updates the distro and the cache, we're only focusing on Debian Servers for now until the playbook is successful then I will divert off to test out with other distros. The kube_deploy_playbook is basically finished since all the work is done via roles which care called out under roles. 



# Conclusions 

I've been having fun learning Ansible, it's based on a simple language of the YAML language which is simple to understand, however playbooks can get complicated pretty quick. 

**A.I. Transparency:** AI was used to make this Ansible Playbooks but ONLY to troubleshoot some errors.

***No AI was used to write this repository.*** 
