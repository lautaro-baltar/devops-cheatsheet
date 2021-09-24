# DevOps Cheatsheet

This repo is meant as a centralization of techonologies, templates and handy-to-have files such as docker compose for various applications.

I don't claim ownership over all the content, every file/service/idea that was provided by someone will be tagged and mentioned as author.

# Current IDEAS [WIP]

## Docker
    - Database + UI:
        - Mongo + Mongo-express
        - MySQL + phpMyAdmin
        - Postgres + PgAdmin
        - Redis + redis commander
    - Tools (WIP)
        - Jenkins
        - grayLog
        - SonarQube
        - Flyway

## Terraform

### AWS modules
    - Jenkins
    - grayLog
    - SonarQube
    - Flyway
    - EC2 Instance + SG + EIP
    - VPC + Subnet
    - VPC + Public sub + Private sub
    - RDS + SG
    - LB + ASG + Node pool + SG
    - Kubernetes Cluster

## Jenkins
    - master - slave architecture
	- pull repo + build services locally in node
	- pull repo + build docker + deploy
	- pull repo + build docker + push registry + update compose + push repo + SSH deploy
	- pull repo + build docker + push registry + update compose + push repo + Terraform deploy
	- pull repo + build docker + push registry + update compose + push repo + kubectl deploy
			

## Install Make on Windows

First we need to install the Chocolatery Package Manager.

- Open a Powershell administrative shell
- Copy and pase the following command:
```
Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; iex ((New-Object System.Net.WebClient).DownloadString('https://chocolatey.org/install.ps1'))
```
- Once installed, test with
``` 
choco or choco -? 
```

Install Make
- Having Chocolatery already installed, run the following command:
```
choco install make
```
