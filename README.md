# challenges-kubernetes

[![Build Status](https://travis-ci.org/DennyZhang/challenges-kubernetes.svg?branch=master)](https://travis-ci.org/DennyZhang/challenges-kubernetes) [![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](http://makeapullrequest.com)

[![LinkedIn](https://raw.githubusercontent.com/USDevOps/mywechat-slack-group/master/images/linkedin.png)](https://www.linkedin.com/in/dennyzhang001) <a href="https://www.dennyzhang.com/slack" target="_blank" rel="nofollow"><img src="http://slack.dennyzhang.com/badge.svg" alt="slack"/></a> [![Github](https://raw.githubusercontent.com/USDevOps/mywechat-slack-group/master/images/github.png)](https://github.com/DennyZhang)

File me [tickets](https://github.com/DennyZhang/challenges-kubernetes/issues) or star [the repo](https://github.com/DennyZhang/challenges-kubernetes).

**Similar Challenges**: https://www.dennyzhang.com/battle

<a href="https://github.com/DennyZhang?tab=followers"><img align="right" width="200" height="183" src="https://raw.githubusercontent.com/USDevOps/mywechat-slack-group/master/images/fork_github.png" /></a>

<a href="https://www.dennyzhang.com"><img src="https://raw.githubusercontent.com/DennyZhang/challenges-kubernetes/master/images/kubernetes.png"/> </a>

Table of Contents
=================
Challenges Your Kubernetes Skills And Knowledge

   * [Scenarios](#scenarios)
      * [Scenario-101: 1-Node K8S Deployment I](#scenario-101-1-node-k8s-deployment-i)
      * [Scenario-102: 1-Node K8S Deployment II](#scenario-102-1-node-k8s-deployment-ii)
      * [Scenario-103: 1-Node K8S Deployment III](#scenario-103-1-node-k8s-deployment-iii)
      * [Scenario-201: 3-Nodes K8S Deployment I](#scenario-201-3-nodes-k8s-deployment-i)
      * [Scenario-202: 3-Nodes K8S Deployment II](#scenario-202-3-nodes-k8s-deployment-ii)
      * [Scenario-301: 3-Nodes Jenkins Deployment I](#scenario-301-3-nodes-jenkins-deployment-i)
      * [Scenario-302: 3-Nodes Jenkins Deployment II](#scenario-302-3-nodes-jenkins-deployment-ii)
   * [Highlights](#highlights)
   * [Contributors: Give People Credits](#contributors-give-people-credits)
   * [License](#license)

<a href="https://www.dennyzhang.com"><img align="right" width="185" height="37" src="https://raw.githubusercontent.com/USDevOps/mywechat-slack-group/master/images/dns_small.png"></a>

# Scenarios

## Scenario-101: 1-Node K8S Deployment I
- Objective: Get familiar with K8S concept. Here K8S stands for Kubernetes.
- Requirements:
```
1. Start one node of k8s in your laptop. Mac or Linux
2. Start a nginx webserver with one instance
3. Scale nginx service into 2 instances.
4. Get familiar with k8s dashboard. Find pods from GUI, check nginx log.
```
- See [kubernetes.yaml](Scenario-101/kubernetes.yaml)
- Main Tech: minikube, nginx, dashboard
- See more: [Scenario-101](./Scenario-101)

## Scenario-102: 1-Node K8S Deployment II
- Objective: Single node deployment for stateful service
- Requirements:
```
1. Use yaml to start one mysql server service with 1 instance.
2. Use yaml to start one mysql client service with 2 instances.
3. Delete the db server instance, make sure a new one will be created automatically.
4. When db server is recreated, make sure no data loss.
```
- See [kubernetes.yaml](Scenario-102/kubernetes.yaml)
- Main Tech: minikube, mysql, volume
- See more: [Scenario-102](./Scenario-102)

<a href="https://www.dennyzhang.com"><img align="right" width="185" height="37" src="https://raw.githubusercontent.com/USDevOps/mywechat-slack-group/master/images/dns_small.png"></a>

## Scenario-103: 1-Node K8S Deployment III
- Objective: Advanced k8s deployment for one single db service
- Requirements:
```
1. Suppose your k8s/minikube have multiple cluster, how you can segrate them? (Hint: namespace)
2. When we initialize mysql via yaml, avoid store mysql root password in plain text. (Hint: secrets)
3. Make sure we can create no more than 1 pods for DB server. (Hint: ResourceQuota)
```
- See [kubernetes.yaml](Scenario-103/kubernetes.yaml)
- Main Tech: minikube, mysql, volume, Job
- See more: [Scenario-103](./Scenario-103)

## Scenario-201: 3-Nodes K8S Deployment I
- Objective: Know how to deployment k8s cluster env
- Requirements:
```
1. Deploy 3 nodes k8s env in your virtualbox.
   One as controller, the other two as worker
2. Deploy k8s web UI, which is missing by default.
3. Create a nginx service with 6 instances.
   They should be balanced across worker nodes.
4. Visit nginx service by loadbalancer. (Hint: Ingress)
```
- Main Tech:
- See more: [Scenario-201](./Scenario-201)
- TODO

## Scenario-202: 3-Nodes K8S Deployment II
- Objective: k8s cluster env with stateful service
- Requirements:
```
1. Deploy 3 nodes k8s. One controller, others as worker
2. Create an elasticsearch service with 4 instances.
   2 as master, 2 as data.
3. Create a nightly job to backup elasticsearch cluster. (Hint: Cron Jobs)
4. If any es instance has crashed, get alerts.
```
- Main Tech:
- See more: [Scenario-202](./Scenario-202)
- TODO
<a href="https://www.dennyzhang.com"><img src="https://raw.githubusercontent.com/DennyZhang/challenges-kubernetes/master/images/k8s_concept3.png"/> </a>

## Scenario-301: 3-Nodes Jenkins Deployment I
- Objective: Real service deployment
- Requirements:
```
1. Deploy 3 nodes k8s. One controller, others as worker
1. Deploy jenkins service with 1 master 2 agents
2. When Jenkins crash, get alerts
```
- Main Tech:
- See more: [Scenario-301](./Scenario-301)
- TODO

## Scenario-302: 3-Nodes Jenkins Deployment II
- Objective: Real service deployment
- Requirements:
```
1. Deploy 3 nodes k8s. One controller, others as worker
2. Deploy Jenkins service by helm
3. Use nginx as an ingress for Jenkins master
4. Simulate Jenkins slave crash events, and confirm service is fine
5. Simulate Jenkins master crash events, and confirm service is fine
```
- Main Tech:
- See more: [Scenario-302](./Scenario-302)
- TODO

# Highlights

- More resources: run services on k8s cluster
```
http://containertutorials.com/get_started_kubernetes/k8s_example.html
Kubernetes Example

https://kubernetes.io/docs/tutorials/
kubernetes kubernetes

https://kubernetes.io/docs/getting-started-guides/scratch/
Creating a Custom Cluster from Scratch

https://github.com/kubernetes/examples
kubernetes examples in GitHub From Google

https://kubernetes.io/docs/concepts/configuration/overview/
Configuration Best Practices
```
<a href="https://www.dennyzhang.com"><img align="right" width="201" height="268" src="https://raw.githubusercontent.com/USDevOps/mywechat-slack-group/master/images/denny_201706.png"></a>

- More resources: k8s cluster itself
```
https://github.com/kelseyhightower/kubernetes-the-hard-way
Bootstrap Kubernetes the hard way on Google Cloud Platform. No scripts.

https://github.com/davidkbainbridge/k8s-playground
Simple VM based Kubernetes cluster setup
```

# Contributors: Give People Credits
Below are folks who have contributed via GitHub!

# License
- Code is licensed under [MIT License](https://www.dennyzhang.com/wp-content/mit_license.txt).

<a href="https://www.dennyzhang.com"><img align="right" width="185" height="37" src="https://raw.githubusercontent.com/USDevOps/mywechat-slack-group/master/images/dns_small.png"></a>
