# HELM

# Table of content 
- [introduce HELM](#intro)
- [problems-with-the-traditional-approach](#problems-with-the-traditional-approach)
- [HELM architecture ](#helm-architecture )



## Intro HELM

Helm helps you manage K8s App

Help charge help you dfine, install, upgrade even the most complex K8s Application 

## Problems with the traditional approach 

Problem1: 

Khi start mot serervice phai thuc hien start tung  service len mot:

kubectl run -f xxx.yaml

kubectl run -f yyy.yaml

- deployploymnet.yaml
- service.yaml

Problem 2:

- install service todo-api with mongodb,
- You need to config mogodb and config mongodb uri to todo-api.yaml

Problem 3:

rollback


You can you use helm to push uri of mongodb to config yaml file


## HELM architecture 