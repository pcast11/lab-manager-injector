# lab-manager-injector

`lab-manager-injector` is an additional component to Lab Manager that installs it in the host system. It sets up prerequisite python3 and pip packages, starts a virtual environment with given requirements, clones the lab-manager repository to the host, and runs the setup file.

## Role Flow

- Ensure pre-requisites are installed
  - Python3 packages
  - Pip3 Packages
- Copy requirements file to target machine
- Create virtual environment for Lab Manager
- Clone Lab Manager to target machine
- Run the Lab Manager setup file

## Requirements

Ansible 2.10 or greater

## Role Variables

Ensure host has Python3 installed.

## Dependencies

None
