---
layout: post
title:  "Ansible - Getting started"
subtitle: "Quick overview of the tool"
date: 2017-03-18 01:00:00
categories: [tech]
---

Simple! Powerfull! Agentless!

Thats right, relatively new kid on the block. Ansible as gained wide popularity. 

Ansible can be used for

 - **Config management**:  is a systems engineering process for establishing and maintaining consistency of a product's performance, functional, and physical attributes with its requirements, design, and operational information throughout its life.
 - **Orchestration**: Orchestration describes automated arrangement, coordination, and management of complex computer systems, and services.
 - **Provisioning**:  as in "provision an environment into which we can deploy services". Can mean spin-up, can mean install debs/rpms on a single machine, can mean run chef client, can mean prep DB servers. "deploy" is then what you do with the output from devs
 - **Continuous Delivery**: Continuous delivery (CD) is a software engineering approach in which teams produce software in short cycles, ensuring that the software can be reliably released at any time. It aims at building, testing, and releasing software faster and more frequently.
 - **App Delopyment**
 - **Security and complaince**

Lets take a look at the ansible architecture

![Ansible Architecure]({{ site.url }}/assets/ansible_architecture.png)

Let's look at the some of the important components of the architecture

#### Playbooks
- Playbooks are
   - Plain-test YAML files that describe desired state of somthing
   - Human and machine readable
   - Can be used to build entire application environments

As shown below Playbooks contain plays that contains tasks composed of modules.

<div class="mermaid">
  graph TD
  subgraph Playbooks
  subgraph Plays
  subgraph Tasks
   modules
  end
  end
  end
</div>

Tasks run sequentially. Tasks can trigger handlers that are run once at the end of plays.

#### Modules

Provided by ansible to help automate nearly every part of environment. Follows the following standard structure.
``` module: directive1=value directive2=value  ```

Dry run or check mode can be used to see if ensible will do what is expected.



#### More to come soon .. stay tuned..