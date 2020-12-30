# CyberArk DAP AWS EKS Integration Lab 2021
This is a tutorial on how to secure secrets of AWS EKS applications by CyberArk Dynamic Access Provider (DAP).   
We will cover deploying DAY Master, DAP follower instances by follower seed fetcher.
Secretless Broker & inital container will also be covered in this tutorial.

Extra tech challenges will be included in each sections for quick learners.

## Overview

EKS is used as platform to host the [demo app](https://github.com/jeepapichet/cityapp)
The application will connect to a MySQL database to retreive data, and during authenication, [secrets](https://docs.cyberark.com/Product-Doc/OnlineHelp/AAM-DAP/Latest/en/Content/Get%20Started/key_concepts/secrets.html) will be used by the application.

[CyberArk Dynamic Access Provider (DAP)](https://docs.cyberark.com/Product-Doc/OnlineHelp/AAM-DAP/Latest/en/Content/Get%20Started/WhatIsConjur.html) is used in this tutorial to secure & manage the secrets.   


## Architecture

![Architecture](https://github.com/QuincyChengAtWork/DAP-OpenShift-Lab-2020/raw/master/images/architecture.png)

## Technical Procedure

### Prerequisite
 - Understand basic Linux installation and administration
 - Unkerstand basic Kubernetes setup and administration
 - Understand basic AWS administration

### [Setup Jump Host](00-Setup_Jump_Host.md)
1. Setup CyberArk CorePAS based on CGD
2. Setup 2 Extra VM (DAP Master & OKD)
3. Onboard MySQL Account to CorePAS
4. Setup DAP Master
5. Configure Vault Synchronizer
