# Install KVM on CentOS 7

## Introduction

> This is an Ansible Playbook used to install KVM on remote servers. This was built specifically for CentOS 7 Linux but could easily be adapted for other Linux Distributions

## Installation

1. Clone this repository
2. Update `inventory` to use your IP address (or DNS) or your machine
3. Verify the correct configuration in `ansible.cfg` exist for your setup
4. execute `ansible-playbook main.yml`
