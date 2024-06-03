**#  2-Tier-App-Deployment-K8s**

This repository contains YAML configuration files for deploying a MySQL database and a Todo application using Kubernetes.

**## Overview**

This project includes the following YAML files:

* `mysql-config.yml`: Defines the configuration of the MySQL database cluster.
* `mysql-deployment.yml`: Deploys the MySQL database pods.
* `mysql-namespace.yml`: Creates a dedicated namespace for the MySQL cluster.
* `mysql-persistentVol.yml`: Defines a persistent volume for the MySQL database data.
* `mysql-secrets.yml`: Stores sensitive information like MySQL credentials.


**## Prerequisites**

* A Kubernetes cluster
* kubectl configured to access the cluster

**## Installation**

1. Clone the repository:

```
git clone https://github.com/Awais411/MySQL-Deployment-K8s.git
```

2. Change directory to the cloned repository:

```
cd your-repo-name
```

3. Apply the YAML files to your Kubernetes cluster:
  ** You must have enough understanding with kubernetes, How it works, the syntax of YAML files and how to make changes according to requirement.**

```
kubectl apply -f mysql-namespace.yml
kubectl apply -f mysql-persistentVol.yml
kubectl apply -f mysql-secrets.yml
kubectl apply -f mysql-config.yml
kubectl apply -f mysql-deployment.yml
kubectl apply -f todo-deployment.yml
```

**## Verification**

Once the YAML files are applied, you can verify the deployment using the following commands:

```
kubectl get pods
kubectl get services
```

**## Contributing**

We welcome contributions to this project. Please follow the standard Git workflow and create pull requests for your changes.


**## Further Resources**

* Kubernetes documentation: [https://docs.kubernetes.io/](https://docs.kubernetes.io/)
* MySQL documentation: [https://dev.mysql.com/doc/](https://dev.mysql.com/doc/)

This README provides a clear overview of the project, installation instructions, verification steps, and contribution guidelines. It also includes references to relevant resources for further exploration.
