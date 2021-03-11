# Ansible Role: Lab Manager Respository Injector

Installs the [Lab Manager Repository](https://github.com/redhat-gpe/rhlearning.lab_manager) for RHEL.

## Requirements

This role only is needed/runs on RHEL and its derivatives.

## Role Variables

Available variables are listed below, along with default values (see `defaults/main.yml`):

__Dependencies for yum__

lab_manager_injector_yum_dependencies_python3: 
  - git 
  - python3-pip 
  - libselinux-python3

__Dependencies for pip__

lab_manager_injector_pip_dependencies: 
  - virtualenv

__Where the virtual environment will be stored__

lab_manager_injector_virtual_env_home: /opt/virtualenvs

___Virtual environment name__

lab_manager_injector_virtual_env_name: venv-lab_manager

__Lab Manager Repo__

lab_manager_injector_git_repo: https://github.com/redhat-gpe/rhlearning.lab_manager.git

__Where Lab Manager will be stored__

lab_manager_injector_home: /opt/lm_repo_clone

__Setup file for the injector__

lab_manager_injector_setup_file: setup.yml

__Git branch to use__

lab_manager_git_branch: main

## Dependencies

Ansible 2.10 and Python 3

## Example Playbook
```yaml
---
- name: Installs the lab manager to a machine
  hosts: host
  become: true
  tasks:
    - name: Call the role
      include_role:
        name: lab-manager-injector
```

