---
layout: post
title:  "Continuous Integration"
subtitle: "Quick review of core concepts"
date: 2017-02-12 01:00:00
categories: [tech]
---

### Recognize the pain, you must!###

_` How long would it take you organization to deploy a change that involved just one line of code? Do you do this on a repeatable, relaible basis ? `_

### Know the priorities. ###

_` Our highest priority is  to satisfy the customer through early and continuous delivery of valuable software  - Agile Manifesto`_

### The Idea!###
_` Cease dependence on mass inspection to achieve quality. Improve the process  and build quality into the product in the first place  - E Edwards Deming`_

### How ? ###

Release frequently in order to

- Feedback from users
- Reduce risk of release
- real project progress

Fast, automated feedback on the production readiness of application everytime there is a change to code, infrastructure or configuration.

### But How ? ###

Deployment Pipeline : An automated implementation of systems's build,deploy,test and release process.

- QA / Testing should be able to test any build on demand by one click.
- Deployment Team should be able to deploy any build by one click

Following diagram shows variaous stages of deployent pipeline and the interaction between them

{% include image name="process_diagram.png" caption="Deployment Pipeline" %}

Everything is automated for fasterfeedback, and down the pipeline evironments become similar to production.

{% include image name="deployment_pipeline.jpg" caption="Deployment Pipeline" %}

### Embrace ###

- Devops
	- Culture
	- Automation
	- Measurement
	- Sharing
- Incrimentalism
- Blue green deployments
- Decouple release and deployment
- Feature toggles
- Make it easy for every one to see what is happening

References - [Continuous Delivery By
Martin Fowler, Jez Humble ](https://yow.eventer.com/events/1004/talks/1062)
