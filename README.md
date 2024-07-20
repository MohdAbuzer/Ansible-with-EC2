## README

# Using Ansible to Dynamically Manage AWS EC2 Instances

This repository contains configurations and guidelines for using Ansible to dynamically manage AWS EC2 instances. By leveraging Ansible's AWS EC2 dynamic inventory plugin, you can automate the discovery and management of EC2 instances in a flexible and scalable manner.


## Introduction

In dynamic cloud environments, efficient infrastructure management is crucial. This repository demonstrates how to use Ansible's AWS EC2 dynamic inventory plugin to discover and manage EC2 instances in real-time. This approach allows for seamless scaling and management of instances based on their state and tags.

## Prerequisites

- Ansible installed on your local machine.
- AWS CLI installed and configured with appropriate credentials.
- An AWS account with EC2 instances.

## Setup

1. Clone the repository:

   ```sh
   git clone https://github.com/MohdAbuzer/Jenkins_CICD_with_ArgoCD.git
   cd Jenkins_CICD_with_ArgoCD
   ```

2. Install the necessary Ansible collections:

   ```sh
   ansible-galaxy collection install amazon.aws
   ```

## Configuration

Create a file named `aws_ec2.yaml` in the `inventory` directory with the necessary configuration for the AWS EC2 dynamic inventory plugin. This file specifies the regions, filters, and groups for managing EC2 instances dynamically.

### Key Configuration Details

- **plugin**: Specifies the AWS EC2 plugin.
- **regions**: Lists the AWS regions to query.
- **filters**: Filters instances based on criteria, such as state.
- **keyed_groups**: Groups instances based on tags or instance IDs.
- **hostnames**: Attributes to use as hostnames for instances.
- **compose**: Defines additional variables, such as the SSH user.

## Usage

To use the dynamic inventory with your playbooks, specify the `aws_ec2.yaml` file as your inventory source when running Ansible commands.



For more detailed information, refer to the full article on Hashnode: [Using Ansible to Dynamically Manage AWS EC2 Instances](https://mohdabuzer.hashnode.dev/using-ansible-to-dynamically-manage-aws-ec2-instances).
