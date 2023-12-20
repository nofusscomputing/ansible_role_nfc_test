---
title: Ansible Testing
description: No Fuss Computings Ansible role nfc_kubernetes
date: 2023-12-17
template: project.html
about: https://gitlab.com/nofusscomputing/projects/ansible/roles/kubernetes
---

This Ansible roles purpose is to enable unit and functional testing of Ansible Playbooks. Tests are declared using a simple yaml file. 


## Features

This role deploys a K3s cluster. In addition it has the following features:

- Unit Testing

    > Designed to test the individual components of a playbook.

    - syntax check of all playbooks

    - more planned

- Functional testing

    > designed to test the functionality of a playbook.

    - _planned feature_

- Mock Roles

- Test Artifacts

- XUnit `xml` test report


## Role Workflow

The role workflow is broken down into stages with `job_tags` being the method of choosing the stage. The workflows are as follows:

1. Test Setup

    1. finds all playbooks

    1. finds all roles used in playbooks

    1. creates mock roles

    1. creates a test fixture

1. Unit Testing

    1. loads test fixture

    1. iterates over all playbooks
    
        1. conducts Syntax Check

    1. stores results in test artifact

1. Functional testing _(planned)_

1. Report Creation

    1. counts passed tests

    1. counts failed tests

    1. creates XUnit `xml` test report


## Default Variables


``` yaml title="defaults/main.yaml" linenums="1"

--8<-- "defaults/main.yaml"

```