# Intro and Comparison

UMU

+   https://idp.umu.se/saml2/idp/SSOService.php?SAMLRequest=fVFbT4MwFP4rpO%2BjhTlkzSDB7cEl0y0DffDFFHaUJtDWnuLl3wtjxpmYvbbf%2FSxQtI3hWedqtYe3DtB5n22jkB8%2FEtJZxbVAiVyJFpC7iufZ3YaHPuPGaqcr3RAvQwTrpFZLrbBrweZg32UFD%2FtNQmrnDHJKsTPWRyUrH4HmtSxL3YCrfURNB82Q7rZ5QbxVH0IqMcj9kuXB%2BF3bDdQhWTg80Dzfnox8UxvirVcJeZ5BcDUvp%2FE8AHYdsaiKIgjnL%2BU0iJioylkPQ%2BxgrdAJ5RISsiCesOmExQWLOQv5jD0Rb3fqdiPVQarXy0OUIwj5bVHsJmOLR7B4bNADSLoYQvOjsT0b%2BLKs%2BFmVpP9tuKBnoqOD4fe9ynq1042svrysafTH0oJwkJCA0HSk%2FL13%2Bg0%3D&RelayState=cookie%3A1520496147_2971
+   ​

## Stacks

+   https://stackshare.io/facebook/facebook
+   https://stackshare.io/google/google
+   https://stackshare.io/uber
+   http://techstacks.io/slack
+   https://www.quora.com/What-is-the-tech-stack-behind-Slack
+   [uber search](https://www.google.ru/search?newwindow=1&ei=cfKgWuzOGszX6QSdkInoCA&q=uber+stack+technology+devops&oq=uber+stack+technology+devops&gs_l=psy-ab.3...9292.9656.0.9790.4.4.0.0.0.0.77.262.4.4.0....0...1c.1.64.psy-ab..0.0.0....0.YuEKN9FlR0Y)
+   [Colabo.Space - DevOps - Diagram](https://www.draw.io/?state=%7B%22folderId%22:%220B-CAPfjq-r7CQ2doV1FZNGwxcGM%22,%22action%22:%22create%22,%22userId%22:%22106768238102316613023%22%7D#G1H3Wc_tMZk6A2FCBybbnnmVnD2aAR8sQx)

## Sources

+   https://wiki.openstack.org/wiki/Fuel
+   [How does your organisation deploy cloud environments? Is it completely automated? Is it completely “Infrastructure as Code”?](https://opencredo.com/cloud-bootstrapping/)
+   [Comparing top DevOps tools: Docker vs Kubernetes vs Puppet vs Chef vs Ansible](https://www.znetlive.com/blog/compare-top-devops-tools-docker-kubernetes-puppet-chef-ansible/)
+   [Vagrant, Docker, Puppet, Chef](https://stackoverflow.com/questions/41471832/vagrant-docker-puppet-chef)
+   [Does Docker make Ansible and similar orchestration tools redundant?](https://www.reddit.com/r/docker/comments/5mfx0e/does_docker_make_ansible_and_similar/)
    +   **Orchestration** is allocating resources to applications
    +   **Config management** is configuring servers. 
    +   **Ansible** isn't an orchestration tool, its config management. It can certainly be used for orchestration. It will work, but it's not ideal. I see people do the same thing with **terraform**. There are very specific use cases for each tool. Using the right tool for the job will save you a lot of pain on the back end.
+   [Marathon, Kubernetes, Docker Compose, Terraform, Puppet, Chef, Ansible, SaltStack, and Juju](https://rhonabwy.com/2016/06/19/marathon-kubernetes-docker-compose-terraform-puppet-chef-ansible-saltstack-and-juju/)
    +   The stand-out challenge that I keep in my mind for this kind of automation is “How can it be used to easily install, configure, run, and **keep running** an instance of **OpenStack** on 3 to 50 physical machines?”


+   **DevOps**, the **software engineering culture** initiated to bring developers and operations together, has now become one of the most essential aspects of **software development lifecycle**. It is now an integral part of project planning till delivery, from startups to large enterprises.
+   The DevOps **automate and monitor** the process of software creation, ranging from **integration**, **testing**, **releasing** to **deploying** and **managing** it. It reduces the development cycles, increases the frequency of deployment, and complements the objectives of a business

## Tools

### Docker

+   http://www.docker.com/
+   It builds on Linux Containers (**LxC**) to create virtual environments, and enables users to create, deploy, run, and manage applications within the **containers**.
+   It has several components, but primarily it is used for "**bundling**" (Note: it does much more than that, but that is an ELI5 answer) software and requires a host system (or infrastructure) to run on. It adds a **little security** to applications but mostly provides a consistent "OS" for an application to run on
+   Docker, allows to **package** an application with all of its dependencies into a **standardized unit of software development**. So, it reduces a friction between developer, QA and testing. It dynamically change your application, adding new capabilities every single day, scaling out services to quickly changing the problem areas.
+   Docker is putting itself in an excited place as the **interface to PaaS** be it networking, discovery and service discovery with applications not having to care about underlying infrastructure.
+   Yes, their are still **issues with docker in production** (thought all major companies already migrated their infrastructure to docker), but, hopefully, we'll see the **solutions** to those problems, as docker team and contributors working hard on those issues.
+   As **Docker Volume driver** allows third-party container data management solutions to provide data volumes for containers which operate on data, such as database, key-value stores, and other stateful applications.
+   Nothing virtual here, simply imagine a real process and required libraries are **sandboxed**, then shipped to the server as an archive. Resource usage is decided upon run command.

#### Docker Compose

### **Chef/Puppet*

-   are the "same", they are **configuration management**
-   While you can use them to manage virtual machines or public/private clouds, most people don't tend to use them that way. They are configuration management. They typically come into play **after a virtual machine is fired up** to get them in a **desired state**.
    -   That is to say, what software is needed on the virtual machine, what users need to be added, what configuration is needed, etc. Thus, it tends to be used for **scaling infrastructure**
-   Can be used to **automate** anything you type in **bash** to make your project setup (except **application keys** etc). You can use them to **build docker images** or **vagrant environments**, so they don't necessarily have to **exist** on physical production server. See [Packer](https://www.packer.io/)

#### Puppet

+   https://puppet.com/
+   It is an **open source configuration management tool**, using which developers and operations teams can securely deliver and operate software (**infrastructure, applications**) anywhere.
+   It enables users to <u>understand and act on the **changes**</u> that take place in applications along with the **in-depth reports and real-time alerts**.
+   Users can identify those changes, and **remediate** the issues.
+   The infrastructure is treated as a **code** by Puppet, which helps in easier reviewing and **testing** of configurations across all the environments- development, test and production.
+   Puppet contains a daemon called **Puppet agent** that runs on the client servers. It has another component which contains configuration for all hosts, called **Puppet master**. The Puppet agent and Puppet master are securely encrypted using the **SSL**.

#### Chef

+   https://www.chef.io/chef/
+   Chef delivers fast, scalable, and flexible IT automation, which automates the **Web-Scale IT**. Chef is also a **configuration management tool** like Puppet, and uses ‘**recipes**’ in the form of instructions for web-server configuration, databases and load balancers.
+   The configuration policy of Chef allows users to define infrastructure as **code**. Its development tools can **test** configuration updates on workstations, development infrastructure, and cloud instances.
+   Chef packages the configurations into JSON files called ‘**cookbooks**’, and runs the software in client-server mode (Chef-server) and ‘Chef-solo’

### Ansible

+   https://www.ansible.com/
+   Ansible is simple yet powerful **server and configuration management tool**, that can transform the DevOps of an organization by modernizing IT and enabling faster deployment of applications.
+   It **automates** configuration management, orchestration, application deployment, cloud provisioning, and a number of other IT requirements.
+   The **difference** between Ansible and the above configuration management tools (Puppet, Chef) is that they probably have a **better set of features**, but Ansible is **far simpler** than them. It is mostly used for **configuration deployment**.
+   It can be used to **make changes** in newly-deployed machines and reconfigure them

### Kubernetes

+   https://kubernetes.io/
+   Where **Docker** provided the first step in helping developers build, ship and run software easily, **Kubernetes** has helped take a giant leap by helping DevOps **run containers in a cluster**, manage applications **across** different containers and **monitor** them effectively as well. It allows vendors to build systems using core Kubernetes technology as it is built on a **modular API core**.
+   Kubernetes is an **open source** system that was developed by **Google**, and was later donated to **CNCF** (Cloud Native Computing Foundation).
+   It helps developers deploy, scale and manage containerized applications with **automation**. 
+   Kubernetes allows DevOps to efficiently fulfill customer’s demands by deploying applications predictably and quickly, **scaling** them, launching new features and **limiting hardware usage** to only the needed resources.
+   Kubernetes is **portable **and can be used with public, private, hybrid, multi-cloud environments; **extensible** with being pluggable, modular, composable, hookable; and is **self-healing** with features like auto-replication, auto-placement, auto-scaling and auto-restart



### Nagios

+   https://www.nagios.org/
+   Nagios is an industry standard tool that helps DevOps teams to **monitor** the desktop and server operating systems, like service **states**, system **metrics**, applications, and services.
+   Nagios provides Nagios XI, Nagios **Log** Server, and Nagios **Network Analyzer** for all the monitoring operations.

### Jenkins

+   https://jenkins.io/
+   It is a self-contained, **extensible automation server** which can be used as **CI** (continuous integration) and **CD** (continuous delivery) server, or can be turned into some **continuous delivery hub** to build, test, deliver or deploy software.

### SaltStack

+   As a side note: SaltStack stands out in this space with the concept of a [reactor](https://docs.saltstack.com/en/latest/topics/reactor/), so it’s intentionally sticking around and listening to what’s happening from within the VM (or VMs) that it’s ‘responsible for’.

### Vagrant

-   Vagrant, while also can be used to manage virtual machines and public/private clouds, is usually only used for **one off environments**. It provides a cohesive file for **creating a virtual machine**. It is similar to chef/puppet that way, but doesn't tend to be used at scale
-   For making development environments spin up on **new developer's machine** in same project, ideally within few minutes. Usually used on top of **virtualbox** but can used with different machine providers
-   Vagrant is a project that helps the **spawning of virtual machines**. It started as an **command line of VirtualBox**, something similar to **Gemfile for VM's**.
-   You can choose the **base image** to start with, **network**, IP, **share folders** and put it all in a file that anyone can **reuse** to spawn the same configured machine. Vagrant has different extensions, provisioning options and VM providers. You can run a VirtualBox, VMware and it is extensible enough to be able to create instances on EC2.

+   Juju
+   Terraform
+   Marathon

## Terraform

-   https://www.terraform.io/
-   Write, Plan, and Create Infrastructure as Code

## Differences

+   Compose, Marathon and Terraform all stop at the level of **declaring the structures**, letting plugins or “something else” orchestrate the coordination for the interesting tasks of a red/green upgrade or rolling upgrade, where 
+   Kubernetes is taking a stab at **including a means of doing just that** within it’s domain of responsibility. The implication in the case of Kubernetes is that developers deploying services with Kubernetes will learn (or know) how the system works and develop code within those constraints – in programmers terms, use it like a **framework**.
+   In the case or Marathon, it expects a developer to tell it what to do – to use it more like a **library**.
+   Kubernetes is **far more opinionated** in this respect, and in a large part betting on the knowledge that it’s development community already has for proving out that it got the right level of abstractions nailed down.
+   A notable difference in Marathon and Kubernetes from Terraform and Compose is that they include an expected **responsibility** to **keep running** and “**keep an eye**” on the ‘applications’/’deployments’ they’re responsible for.
+   Puppet, Chef, Ansible, and SaltStack are all focused on the world of **configuring services within a single** virtual (or physical) machine – the “**install and configure**” and “**start it running**”
    +   and didn’t include the concept of handling a **failure of the machine**
    +   these systems were created **long before cloud computing** was a reality, and the idea of asking for another machine wasn’t a few seconds of work behind an API

### Kubernetes (K8s) vs Docker Swarm

+   [Kubernetes vs Docker Swarm](https://platform9.com/blog/kubernetes-docker-swarm-compared/)
+   [Swarm mode overview](https://docs.docker.com/engine/swarm/)
+   ​

## Scenarios

Scenario 1 ([src](https://stackoverflow.com/questions/41471832/vagrant-docker-puppet-chef))

+   In practice, all of these can be utilized in an environment. Here is an example:
+   Say you have application ***FunTime***. You have eight developers who contribute to this, and FunTime is designed to be ran on a scaleable infrastructure on **AWS**. It is designed to have a **front-end** (FunTime-Front) and a **back-end** (FunTime-API), and requires **postgres**. 4 developers work on the front end, four developers work on the backend. I would do the following (there are many ways to skin this cat, but this is one example):
+   I would use **Docker** for FunTime-Front and FunTime-API. 
+   I would use **Vagrant** to set up a dev environment for the developers (so that they can tweak various components). Vagrant would: **start up the VM locally** (or on a cloud if needed), Install **docker**, pull down the **docker images** for FunTime-Front and FunTime-API, **install postgres**, and **populate postgres** with dummy data, configure network ports to the various components
+   Now the developer has the **full FunTime stack** on their local machine and doesn't have to screw around with configuring anything themselves: they can just type "***vagrant up***".
+   On the **infrastructure side**, I would use **chef (or puppet)** to **configure** the **Environments**: Production, Stage, and Development (or whatever is needed), then chef would **install docker** on the **"application" servers**, "**postgres**" on the **postgres servers**, apply **security settings**, etc. In this way all the related servers are the same. If I needed to **update a server or add a patch**, it would be trivial with configuration management.
+   In all cases **Docker** would be used so that there is **no application difference** between environments, including the **developers work station**.
+   This would make sure that you don't hear the excuse "Well, it works on my local machine!" very often. In addition, if there is a bungled deployment, **rolling back** the application would be VERY easy with Docker.
+   I hope that provides a little more insight into how they could be used

Scenario 2 ([src](https://www.reddit.com/r/docker/comments/5mfx0e/does_docker_make_ansible_and_similar/))

+   1
    +   In the beginning there was nothing. No servers, no applications, no network, nothing. We need to provision some resources. In steps **terraform**.
    +   First we define a VPC, then some vlans, then an internet gateway, then some security groups. Now we have a basic network. 
    +   Now our servers can talk, but we don't have any servers. So now we define some server resources, but how do we configure them? We could run bash scripts with a local provisioner, but this puts us in a bit of a bind of we ever need to make changes to existing infrastructure. It also means we have to write bash scripts, which generally make it a huge pain in the ass to achieve idempotency.
    +   In steps **Ansible**. Ansible allows you to configure your servers in an **idempotent**, repeatable manner (**same with chef, puppet, etc**). With this, you install your **kubernetes cluster**, configure **certificates**, configure **ssh keys** or LDAP, install **patches**, etc. 
    +   When your **config changes**, or you need to **upgrade kube**, **add users**, or anything else, you just kick off a **config management run**. **Idempotency** means you only change the things that need changing. This way you don't have to **<u>destroy</u>** your entire cluster every time you update.
    +   Now you have your kubernetes cluster up and running, so you can let **kubernetes orchestrate** your containers onto the cluster


+   2

    +   At edX we are experimenting with moving **from EC2 instances** (and AMIs) for production, and **Vagrant** for local development, to **containers for both**.
    +   We can use the **same Ansible** to provision all three. Even if we **fully move to containers**, I suspect we will **continue to use Ansible** as it provides the **freedom** for us, and our open source users, to deploy to **almost any platform**.
    +   Putting all of the orchestration in **`Dockerfile`** is just a step above writing a bash script. If you choose to **change your OS** (e.g. from Debian to Redhat) any **OS-specific code** will need to change. Ansible, and other orchestration software, usually do a good job of obfuscating these customizations.

+   3

    +   It is true that **many docker features kind of make ansible obsolete**. Or rather: have the potential to do so.
    +   As previously pointed out, **docker is a high moving target** which works great in environments with a high change rate. It kind of blows for setting up systems that run for years with little change. So there is room for both and I would not be surprised to see ansible add features that allow you to push and move containers around. Ansible is awesome for its simplicity, docker, especially when clustered.. Not so much.

+   4

    +   If all your apps are Dockerized, it just means you aren't doing **heavy provisioning** now. That's all in the dockerfile/compose. **Ansible now just does the orchestration of the docker cluster/environment management processes**.
    +   With **kubernetes** on coreos (kube-AWS), I'm no longer configuring a base AMI and packages now that CoreOS is the OS, but managing the AWS keypair, KMS keys, Route53 records supporting the multiple kube-aws runs for different regions/environments is **still very much Ansible's useful wheelhouse**.

+   5

    +   Yes, that is kind of true. Ansible/Puppet/Chef/SaltStack is designed for the **old pet-centric world** with **manual installed** and managed servers, VM and OS.
    +   In the new **hyperscale micro service oriented world** consisting of <u>**application containers that are immutable and atomic units**</u>. The usefulness of these **automations tools are limited**. They can still be used on the host nodes and for application testing or function testing.

+   6

    +   I actually use **Ansible** to provision my Docker hosts, and often my top level server containers (Rancher for e.g.).
    +   But then from that point I'll typically use the **tools provided** from that point, be it **compose** files or what have you.
    +   I think there is some merit in using something like **Ansible** if you have an **infrastructure driven by variables** rather than fixed configuration files - but it's not something I've needed so far.
        +   You will the moment you want to **spin up another production cluster** or test out a fix on a **newer version of swarm/kube/mesos** or when you want **multiple DCs/regions** to have identical (and sanely managed) clusters in different places.
        +   **Vars files** for me are now like region, instance size, number of minions, keypair, and friendly env name ("dev" or "prod"). I use Ansible to make **templated, per-environment `cluster.yaml`** files to feed into **kube-AWS**. Works very smoothly.

+   7

    +   At my work, **docker is not yet mature enough to handle certain complex environments**. We ran into a lot of **problems with docker, particularly with dependency management** that made it unusable for **development**. However, it's **amazing for production** and we use it for exactly that. For development though, we stuck to **vagrant / ansible** environments. They just allow much **finer control** and are much more mature and well documented at this point.
        +   So, we have a dependency that can **only have one running instance** of itself on a server at a given time for security reasons, or else it throws an error. Because of this, we have to **`npm link`** any services that require it to a **single repo** on the server. This seems simple enough to fix but it causes **absolute hell in production with docker**, and even **more hell in development**. It's difficult enough to deal with on a host machine, let alone in a docker environment. Vagrant **and Ansible afforded us enough fine tuned control**, but it still took a while to get it running right.
        +   Life pro tip, micro services sound cool on paper but they can be a massive pain in the ass haha.

+   8

    +   **Dockerfiles** are like **bad bash scripts**, RUN do something && because intermediate containers && because some other thing. we create **ansible roles** which **build inside our docker containers**
    +   Our dockerfile is nothing more than **ansible-playbook playbookname.yml** and the standard docker bits, benefit being our **same ansible role works outside of a container on VM or physical or another container (LXC, Rocket, Systemd)**
    +   You might find your doing something wrong later down the road but your obviously not there yet :)

    ​

    ​

# Orchestration

## Kubernetes

+   [How is Kubernetes (k8s) different from Docker?](https://www.quora.com/How-is-Kubernetes-k8s-different-from-Docker)
    +   But the single largest difference between the docker approach and Kubernetes is the **networking model**.
        +   Docker has embraced the **Container Network Model (CNM)** and is expressed through ***`libnetwork`*** (in the docker engine iteself) while 
        +   Kubernetes has embraced **Container Network Interface (CNI)**. There’s not enough room to explain the differences here - but they are significant.
+   THE CONTAINER NETWORKING LANDSCAPE: ***CNI*** FROM COREOS AND ***CNM*** FROM DOCKER
+   Self-Hosted Kubernetes

### KubeNow

https://github.com/kubenow/KubeNow

### OpenStack

+   [youtube - Which is the best way to install Kubernetes on OpenStack?](https://www.openstack.org/videos/sydney-2017/which-is-the-best-way-to-install-kubernetes-on-openstack)
    +   Kubernetes has become a de facto standard for container orchestration engines.But it's difficult to choose the way to install Kubernetes on OpenStack which you want, because there are so many tools and ways to deploy Kubernetes such as following:
        +   Kops
        +   Kubeadm
            +   https://kubernetes.io/docs/admin/kubeadm
            +   https://github.com/kubernetes/kubernetes/tree/master/cmd/kubeadm
        +   Kubespray
        +   Rancher
        +   Tectonic
            +   https://coreos.com/tectonic
        +   Magnum
    +   Each tool have advantages and disadvantages respectively.For example, 
        +   **magnum** is the most easiest way to deploy Kubernetes on OpenStack, however it is often <u>not offered at your OpenStack cloud</u>.
        +   **Kops** is a <u>official</u> way in Kubernetes community, but it <u>doesn't support OpenStack</u>, and so on.
    +   In this session, we will provide the pros and cons from several viewpoints (such as architecture and support status) to select the optimum way to install Kubernetes in your OpenStack environment for troubling OpenStackers
    +   remora
        -   https://github.com/nec-openstack/remora
+   [Easily deploy a Kubernetes cluster on OpenStack](https://cloudbase.it/easily-deploy-a-kubernetes-cluster-on-openstack/)
    +   **Magnum** and **Heat** need to be deployed alongside other OpenStack services such as Nova or Neutron
    +   https://cloudbase.it/easily-deploy-a-kubernetes-cluster-on-openstack/
+   [Deploying Kubernetes on OpenStack using Heat](http://alesnosek.com/blog/2016/06/26/deploying-kubernetes-on-openstack-using-heat/)

### OpenStack on Kubernetes

+   stackanetes
    +   Deploy and manage OpenStack on Kubernetes
    +   https://github.com/stackanetes/stackanetes

### Minikube

+   [Running Kubernetes Locally via Minikube](https://kubernetes.io/docs/getting-started-guides/minikube/)
+   [github - minikube](https://github.com/kubernetes/minikube)
+   [kubernetes - Hello Minikube](https://kubernetes.io/docs/tutorials/stateless-application/hello-minikube/)

# Containers

## Docker

Docker is an open platform for building, shipping and running **distributed applications**. It gives programmers, development teams, and operations engineers the **common toolbox** they need to take advantage of the distributed and networked nature of modern applications.

([src](https://semaphoreci.com/community/tutorials/dockerizing-a-python-django-web-application)) Put simply, Docker gives you the ability to run your applications within a controlled environment, known as a **container**, built according to the instructions you define. A container leverages your machines resources much like a traditional **virtual machine (VM)**. However, containers differ greatly from traditional virtual machines in terms of system resources.

Once Docker is installed, you create a container with a few commands and then execute your applications on it via the **`Dockerfile`**.

Furthermore, Dockerfiles can be **shared** for others to build containers and **extend** the instructions within them by basing their container image on top of an existing one. The containers are also highly **portable** and will run in the same manner regardless of the host OS they are executed on.

[Docker builder instructions info](https://docs.docker.com/engine/reference/builder/): [FROM](https://docs.docker.com/engine/reference/builder/#from),  [RUN](https://docs.docker.com/engine/reference/builder/#run), [COPY](https://docs.docker.com/engine/reference/builder/#copy), and [WORKDIR](https://docs.docker.com/engine/reference/builder/#workdir), [ADD](https://docs.docker.com/engine/reference/builder/#add)

Docker commands:

```sh
# build from the local Dockerfile
docker build .

# show existing docker images
docker images
# remove image
docker rmi <id>

# show containers
docker ps -q -a
# remove container
docker rm <id>

# run docker image, with a name (let's use ubuntu):
docker run -i -t ubuntu:12.04 /bin/bash
#run docker image, without a name, just using the ID:
docker run -i -t 5440ca5be5a4 /bin/bash
```

More info:

+   [How to remove unused Docker containers and images](https://gist.github.com/ngpestelos/4fc2e31e19f86b9cf10b)
+   [Run a Docker Image as a Container](https://stackoverflow.com/questions/18497688/run-a-docker-image-as-a-container)
+   [SSH into a Container](http://phase2.github.io/devtools/common-tasks/ssh-into-a-container/)
+   [How to get bash or ssh into a running container in background mode?](https://askubuntu.com/questions/505506/how-to-get-bash-or-ssh-into-a-running-container-in-background-mode)

### Integrations

+ Docker announced Docker Swarm integration with Kubernetes too:
  + https://www.docker.com/kubernetes

### Python

#### Python Image

```sh
# create python requirements
touch requirements.txt
create a docker file Dockerfile
touch Dockerfile
```

create the ***Dockerfile*** with the content:

```dockerfile
# use the prebuilt Python image
FROM python:2.7
```

run build:

```sh
# build docker from the Dockerfile
docker build .
# see images available
docker images
```

```dockerfile
FROM python:2.7
# the build directory
RUN mkdir build
# set it as working directory
WORKDIR build
# copy requirements.txt to the working directory
COPY ./requirements.txt .
# install all python requirements
RUN pip install -r requirements.txt
# Set the environment variable PYTHONUNBUFFERED
# ENV PYTHONUNBUFFERED 1
# Copy all the files from the project’s root to the working directory
# COPY . .
# EXPOSE 5000
# ENTRYPOINT ["python", "app.py"]
```

#### Docker compose

Create the file **`docker-compose.yml`**:

```
touch docker-compose.yml
```



#### Dockerize your Python Application

[src](https://runnable.com/docker/python/dockerize-your-python-application)



#### More info:

+   [Python + Docker: From development to production: Episode I](https://medium.com/@yoanis_gil/python-docker-from-development-to-production-episode-i-427674710f3e)
+   specialized/from the perspective of provides
    +   pipelines.puppet.com
        +   [Build and Deploy a Python Web App on Docker](https://pipelines.puppet.com/docs/tutorials/build-and-deploy-python-with-docker/)
    +   semaphoreci.com
        +   [Continuous Deployment of a Python Flask Application with Docker and Semaphore](https://semaphoreci.com/community/tutorials/continuous-deployment-of-a-python-flask-application-with-docker-and-semaphore)
        +   [Dockerizing a Python Django Web Application](https://semaphoreci.com/community/tutorials/dockerizing-a-python-django-web-application)

### MySQL

+   [7.7.2 More Topics on Deploying MySQL Server with Docker @ MySQL](https://dev.mysql.com/doc/mysql-installation-excerpt/5.7/en/docker-mysql-more-topics.html)
+   https://hub.docker.com/_/mysql/
+   https://hub.docker.com/r/mysql/mysql-server/
+   https://github.com/sameersbn/docker-mysql
+   [Creating a docker mysql container with a prepared database scheme](https://serverfault.com/questions/796762/creating-a-docker-mysql-container-with-a-prepared-database-scheme)
+   [How to deploy and use a MySQL Docker container](https://www.techrepublic.com/article/how-to-deploy-and-use-a-mysql-docker-container/)
+   [Docker MySQL: create new user](https://stackoverflow.com/questions/39328257/docker-mysql-create-new-user)
+   [[MYSQL] Create database and import sql file with Dockerfile](https://forums.docker.com/t/mysql-create-database-and-import-sql-file-with-dockerfile/30300)

### NodeJS

+   Official Docker Image for Node.js
    +   https://hub.docker.com/_/node/
    +   https://github.com/nodejs/docker-node
+   Yarn
    +   It seems not necessary, since yarn comes with node.js image now
    +   https://hub.docker.com/r/kkarczmarczyk/node-yarn/

### Ghost

+   OFFICIAL REPOSITORY
    +   https://hub.docker.com/_/ghost/
    +   Ghost is a free and open source blogging platform written in JavaScript



# Open Stack

## Hypervisors

+   [Has KVM Won the OpenStack Hypervisor War? (If you can call it a war!)](https://www.leostream.com/blog/has-kvm-won-the-openstack-hypervisor-war-if-you-can-call-it-a-war)
    +   What **hypervisors** does OpenStack support?
        +   OpenStack Compute (**Nova**) runs on a variety of hypervisors, including those from VMware, Citrix, and Microsoft, to name a few. To date, however, OpenStack’s strength-in-numbers lies in **KVM**. Various surveys (such as this one in OpenStack Superuser) show that the majority of OpenStack deployments, at **nearly 90%**, are based on KVM.
        +   Why is that? **KVM turns the Linux kernel into a hypervisor**, and comes standard with many Linux distributions. OpenStack is also a Linux distribution, so the marriage of OpenStack with KVM makes sense. Use your open source software to manage your open source hypervisor! Consequently, the OpenStack community embraced KVM and turned it into the most highly tested and feature rich hypervisor to use in an OpenStack cloud.
+   [Wiki - KVM (Kernel-based Virtual Machine)](https://en.wikipedia.org/wiki/Kernel-based_Virtual_Machine)
    +   **Kernel-based Virtual Machine** (**KVM**) is a [virtualization](https://en.wikipedia.org/wiki/Virtualization) infrastructure for the [Linux kernel](https://en.wikipedia.org/wiki/Linux_kernel) that turns it into a [hypervisor](https://en.wikipedia.org/wiki/Hypervisor). It was merged into the Linux kernel mainline in kernel version 2.6.20, which was released on February 5, 2007.[[1\]](https://en.wikipedia.org/wiki/Kernel-based_Virtual_Machine#cite_note-2620notes-1) 
    +   KVM requires a processor with [hardware virtualization extensions](https://en.wikipedia.org/wiki/Hardware-assisted_virtualization).[[2\]](https://en.wikipedia.org/wiki/Kernel-based_Virtual_Machine#cite_note-2) KVM has also been ported to [FreeBSD](https://en.wikipedia.org/wiki/FreeBSD)[[3\]](https://en.wikipedia.org/wiki/Kernel-based_Virtual_Machine#cite_note-3) and [illumos](https://en.wikipedia.org/wiki/Illumos)[[4\]](https://en.wikipedia.org/wiki/Kernel-based_Virtual_Machine#cite_note-4) in the form of loadable kernel modules.
+   [openstack - kvm](https://docs.openstack.org/mitaka/config-reference/compute/hypervisor-kvm.html)
+   xhyve
    +   https://github.com/mist64/xhyve
        +   xhyve, a lightweight OS X virtualization solution
        +   The *xhyve hypervisor* is a port of [bhyve](http://www.bhyve.org/) to OS X. It is built on top of [Hypervisor.framework](https://developer.apple.com/library/mac/documentation/DriversKernelHardware/Reference/Hypervisor/index.html) in OS X 10.10 Yosemite and higher, runs entirely in userspace, and has no other dependencies. It can run FreeBSD and vanilla Linux distributions and may gain support for other guest operating systems in the future.
    +   [Lightweight Virtualization on OS X Based on bhyve](http://www.pagetable.com/?p=831)
        +   [xhyve](https://github.com/mist64/xhyve) is a lightweight virtualization solution for OS X that is capable of running Linux. It is a port of FreeBSD’s [bhyve](http://bhyve.org/), a KVM+QEMU alternative written by Peter Grehan and Neel Natu.
        +   xhyve may make a good solution for running Docker on your Mac, for instance.

## Comparison

+   [2015 - What is difference between docker, puppet, chef and vagrant?](https://www.quora.com/What-is-difference-between-docker-puppet-chef-and-vagrant)
+   [deployment-tool-ansible-puppet-chef-salt.md](https://gist.github.com/jaceklaskowski/bd3d06489ec004af6ed9)
+   [Sep 26, 2016 - Why we use Terraform and not Chef, Puppet, Ansible, SaltStack, or CloudFormation](https://blog.gruntwork.io/why-we-use-terraform-and-not-chef-puppet-ansible-saltstack-or-cloudformation-7989dad2865c)
+   [Nov 8, 2016 - PUPPET VS ANSIBLE VS DOCKER COMPARISON](https://www.linuxnix.com/puppet-vs-ansible-vs-docker-comparison/)
+   [September 27, 2016 - Puppet vs. Chef vs. Ansible vs. SaltStack](https://www.intigua.com/blog/puppet-vs.-chef-vs.-ansible-vs.-saltstack)
+   [June 19, 2016 - Marathon, Kubernetes, Docker Compose, Terraform, Puppet, Chef, Ansible, SaltStack, and Juju](https://rhonabwy.com/2016/06/19/marathon-kubernetes-docker-compose-terraform-puppet-chef-ansible-saltstack-and-juju/)

## Vagrant

+   https://www.vagrantup.com/
+   Vagrant is a tool for **building and managing virtual machine environments** in a single workflow. With an easy-to-use workflow and focus on automation, Vagrant lowers development environment setup time, increases production parity, and makes the "works on my machine" excuse a relic of the past.
+   If you are already familiar with the basics of Vagrant, the [documentation](https://www.vagrantup.com/docs/index.html) provides a better reference build for all available features and internals.
+   http://docs.ansible.com/ansible/latest/guide_vagrant.html
+   https://www.vagrantup.com/docs/provisioning/ansible.html

## Chef

+   Achieve speed, scale, and consistency by automating your infrastructure with Chef
+   Cookbooks
    +   https://github.com/chef-cookbooks/docker
    +   https://github.com/chef-cookbooks/mysql
    +   https://github.com/chef-cookbooks/nginx

## Puppet

+   https://puppet.com/
+   https://puppet.com/products/how-puppet-works
+   https://puppet.com/products/emulator
+   https://puppet.com/download-learning-vm

## HEAT

[HEAT or Ansible in OpenStack? Both!](http://software.danielwatrous.com/heat-or-ansible-in-openstack-both/)

**HEAT** is designed to capture details related to infrastructure and accommodate provisioning of that infrastructure on OpenStack. **CloudFormation** does the same thing in AWS and **Terraform** is an abstraction that has providers for both OpenStack and AWS (and many others).

## CloudInit

+   https://cloud-init.io/
+   http://cloudinit.readthedocs.io/en/latest/
+   [Provide user data to instances @ OpenStack](https://docs.openstack.org/nova/latest/user/user-data.html)
+   [Launch an instance from an image @OpenStack](https://docs.openstack.org/ocata/user-guide/cli-nova-launch-instance-from-image.html)
+   [Using Cloud-Init in an OpenStack Environment to Automate the Initialization of vSRX Instances](https://www.juniper.net/documentation/en_US/vsrx/topics/task/configuration/security-vsrx-cloud-init-support.html)

***Cloud-init*** is the [Ubuntu package](https://launchpad.net/ubuntu/+source/cloud-init) that handles early initialization of a cloud instance. It is installed in the [Ubuntu Cloud Images](http://cloud-images.ubuntu.com/releases/) and also in the official Ubuntu images available on **EC2**.

Some of the things it configures are:

-   setting a default locale
-   setting hostname
-   generate ssh private keys
-   adding ssh keys to user's .ssh/authorized_keys so they can log in
-   setting up ephemeral mount points

cloud-init's behavior can be configured via **user-data**. [User-data](http://developer.amazonwebservices.com/connect/entry.jspa?externalID=1085) can be given by the user at instance launch time. This is done via the `--user-data` or `--user-data-file` argument to [ec2-run-instances](http://docs.amazonwebservices.com/AWSEC2/latest/CommandLineReference/ApiReference-cmd-RunInstances.html)

***User data*** is a blob of data that the user can specify when they launch an instance. The instance can access this data through the metadata service or config drive. Commonly used to pass **a shell script** that the instance runs on boot.

For example, one application that uses user data is the [**cloud-init**](https://help.ubuntu.com/community/CloudInit) system, which is an open-source package from Ubuntu that is available on various Linux distributions and which handles ***early initialization of a cloud instance***.

You can place user data in a local file and pass it through the **`—user-data <user-data-file>`** parameter at instance creation.

```
$ openstack server create --image ubuntu-cloudimage --flavor 1 \
  --user-data mydata.file VM_INSTANCE
```

## Ansible

Ansible is an open source  IT-automation engine that can be used to automate provisioning, configuration and deployment of cloud resurces. 

+   https://www.ansible.com/
+   What is Ansible?
    +   https://www.ansible.com/resources/videos/quick-start-video
+   https://docs.ansible.com/
    +   http://docs.ansible.com/ansible/modules_by_category.html
    +   http://docs.ansible.com/ansible/playbooks_roles.html
+   https://galaxy.ansible.com/
+   [YouTube - What is Ansible? A short DevOps Introduction](https://www.youtube.com/watch?v=xMHVvHZ-Zn4)
+   [Ansible vs Ansible Tower](https://www.upguard.com/articles/ansible-vs.-ansible-tower)
    +   Ansible Tower is a web-based interface for managing Ansible
+   [COMING SOON: NETWORKING FEATURES IN ANSIBLE 2.5](https://www.ansible.com/blog/coming-soon-networking-features-in-ansible-2.5)
+   Yaml
    +   [YAML Syntax @ ansible](http://docs.ansible.com/ansible/latest/YAMLSyntax.html)
+   Roles
    +   testing
        +   https://github.com/metacloud/molecule
+   IP
    +   [Ansible: get current target host's IP address](https://stackoverflow.com/questions/39819378/ansible-get-current-target-hosts-ip-address)
    +   http://docs.ansible.com/ansible/latest/playbooks_filters_ipaddr.html
+   variables
    +   http://docs.ansible.com/ansible/latest/playbooks_variables.html
+   playbooks
    +   http://docs.ansible.com/ansible/latest/playbooks.html
+   examples
    +   language
        +   https://github.com/ansible/ansible-examples/tree/master/language_features
    +   playbooks
        +   https://github.com/ansible/ansible-examples
        +   Deploying a sharded, production-ready MongoDB cluster with Ansible
            +   https://github.com/ansible/ansible-examples/tree/master/mongodb

### MongoDB

+   [Creating mongodb database with ansible playbook](https://dba.stackexchange.com/questions/185240/creating-mongodb-database-with-ansible-playbook/187759)
+   [how do I create a collection in mongoDB using an Ansible playbook?](https://stackoverflow.com/questions/25562078/how-do-i-create-a-collection-in-mongodb-using-an-ansible-playbook)
+   [Creating a Mongo cluster in AWS with Ansible](https://medium.com/7factor/creating-a-mongo-cluster-in-aws-with-ansible-b97c36f55586)
+   roles
    +   https://github.com/William-Yeh/ansible-mongodb

### MySQL

+   [mysql_db - Add or remove MySQL databases from a remote host](http://docs.ansible.com/ansible/latest/mysql_db_module.html)
+   http://docs.ansible.com/ansible/latest/list_of_database_modules.html#mysql
+   [Properly install MySQL on production server using ANSIBLE](http://techwatch.keeward.com/geeks-and-nerds/properly-install-mysql-on-production-server-using-ansible/)
+   [Install MySQL with ansible on ubuntu](https://stackoverflow.com/questions/26597926/install-mysql-with-ansible-on-ubuntu)
+   roles
    +   https://github.com/bennojoy/mysql
    +   https://github.com/ANXS/mysql

### Nodejs

+   [Installing NodeJS LTS for Ansible](https://stackoverflow.com/questions/45840664/installing-nodejs-lts-for-ansible)
+   roles
    +   https://github.com/nodesource/ansible-nodejs-role
    +   https://github.com/geerlingguy/ansible-role-nodejs

### Ghost

+   https://docs.ghost.org/docs/install
+   roles
    +   https://github.com/mtpereira/ansible-ghost
    +   https://github.com/reactiveops/ansible-ghost

### Openstack

+   Cloud Modules - Openstack
    +   http://docs.ansible.com/ansible/latest/list_of_cloud_modules.html#openstack

#### Keys

-   [Generating a new SSH key and adding it to the ssh-agent](https://help.github.com/articles/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent/)
-   [Specifying ssh key in ansible playbook file](https://stackoverflow.com/questions/44734179/specifying-ssh-key-in-ansible-playbook-file)
-   [how to define ssh private key for servers fetched by dynamic inventory in files](https://stackoverflow.com/questions/33795607/how-to-define-ssh-private-key-for-servers-fetched-by-dynamic-inventory-in-files)

Procedure:

-   generate a new key pair for ansimble through the open cloud interface
    -   or generate a **SSH key-pair**, # ssh-keygen –t rsa
-   download the private key and store it safely as `orchestration-iaas-no.pem`

#### Orchestration

You have to have at least two machines/nodes. One for Ansible running (either local or on the cloud) and other (on the cloud) to deploy with Ansible on.

Regarding the speed and collaboration-wise it is better to have both orchestration node on the OpenStack as well

-   `orchestrator`
-   `colabo-space-1`

Open the `<ansible-project>/hosts` file and fill the **private IP addresses** of nodes and private key locations:

```sh
# each speciffic host
orchestrator ansible_ssh_host=158.39.75.31 ansible_ssh_private_key_file=~/.ssh/orchestration-iaas-no.pem
colabo-space-1 ansible_ssh_host=158.39.75.120 ansible_ssh_private_key_file=~/.ssh/orchestration-iaas-no.pem
colabo-ghost ansible_ssh_host=158.39.75.121 ansible_ssh_private_key_file=~/.ssh/orchestration-iaas-no.pem

# groups
[orchestrators]
orchestrator ansible_connection=local ansible_user=ansible

[colabo-spaces]
colabo-space-1 ansible_connection=ssh ansible_user=ansible

[colabo-ghosts]
colabo-ghost ansible_connection=ssh ansible_user=ansible
```

##### Node configuration

###### Accounts

Create the ansible account on orchestrator node and each node we want to access from ansible

-   Add the orchestration **public key** to all  “**authorized_keys**” file
-   Make sure you **can login** to the machines
-   Also check that the user account has the “**sudo**” privileges

###### Python

Each node should have at least python and python-simplejson

**NOTE**:

+   Ansible’s “raw” module (for executing commands in a quick and dirty way) and the script module don’t even need that. So technically, you can use Ansible to install python-simplejson using the raw module, which then allows you to use everything else.


+   If you need to bootstrap these remote systems by installing Python 2.X, using the ‘raw’module will be able to do it remotely. For example, would install Python2.X and the simplejson module needed to run ansible and its modules.

```sh
#for ansible user
joe ~/.ssh/orchestration-iaas-no.pem
chmod 0600 ~/.ssh/orchestration-iaas-no.pem
```

##### Install ansible on orchestrator

copy the `<ansible-project>` directory to the orchestrator node

Run the ***`install_ansible.sh`*** script

```sh
chmod a+x install_ansible.sh
./install_ansible.sh
```

or 

```sh
# NOTE: The code assumes Ubuntu VMs
# configure the PPA
sudo apt-get update
# On older Ubuntu distributions, “software-properties-common” is called “python- software-properties”
sudo apt-get install software-properties-common
sudo apt-add-repository ppa:ansible/ansible

#install ansible
sudo apt-get update
sudo apt-get install ansible
```

+   copy the private key to the orchestrator node under ansimble user account `~/.ssh/orchestration-iaas-no.pem`
    +   set its access rights to `0600`

#### Testing

Goto `<ansible-project>` directory and **execute** the following command:

```sh
# pinging
ansible -m ping -i hosts colabo-space-1 --private-key ~/.ssh/orchestration-iaas-no.pem
ansible -m ping -i hosts colabo-spaces --private-key ~/.ssh/orchestration-iaas-no.pem
ansible -m ping -i hosts all --private-key ~/.ssh/orchestration-iaas-no.pem

# echo
ansible -i hosts all -a "/bin/echo hello"

# spark
ansible-playbook -i hosts -s playbooks/spark-deployment.yml --private-key ~/.ssh/orchestration-iaas-no.pem
# The complete deployment will take approximately 20 to 30 minutes. Once the installation is finished you can check the cluster status using the following URL: http://<floating-IP-sparkmaster>:8080
```

### Questions:

1.  What language is used by Ansible to define the configurations? 
    .	Can Ansible be used with different Linux distributions? 
    .	What is Ansible inventory file?
    .	What is the major difference between CloudInit vs Ansible-based resource contextualization?
    .	Explain how Ansible works and suggest, within the scope of this task, what is still left to automate?  

## Deployment

+ kubernetes openstack
+ grpc openstack

### npm packages

+ [npm install private github repositories by dependency in package.json](https://stackoverflow.com/questions/23210437/npm-install-private-github-repositories-by-dependency-in-package-json)


+ Cloud Native
  + Computing Foundation
+ Docker
  + Container
+ Kubernetes
  + Orchestration
+ HELM
  + Package and deply
+ Prometheus
  + Monitoring
  + data store
  + visualization
    + graphit
    + graphona
      + dashboard build support
      + alerts 
+ Opentracing
  + distributed tracing



Google

+ **Kubernetes**
  + rewritten OS friendly Borg
    + Borg
      - containers
  + written in Go
  + moves you from dealing with machines into dealing with cluster
+ **gRPC**
  + rewritten Stubby but using HTTP2 and protocol buffer 3
    + Stubby
      - RPC between containers
+ Johny5
  + node for IoT



Videos

+ [Building high performance microservices with Kubernetes, Go, and gRPC (Google Cloud Next '17)](https://www.youtube.com/watch?v=YiNt4kUnnIM)
+ [Docker Swarm or Kubernetes or Mesos - pick your framework! by Arun Gupta](https://www.youtube.com/watch?v=1dgUXNVQS5o)
+ [Mesos vs Kubernetes vs Swarm: Fight! by Christophe Furmaniak](https://www.youtube.com/watch?v=DuGZ5UYHxI8)



+ [Four Distributed Systems Architectural Patterns by Tim Berglund](https://www.youtube.com/watch?v=tpspO9K28PM)
+ [The hardest part of microservices is your data](https://www.youtube.com/watch?v=MrV0DqTqpFU)
+ [Managing Data in Microservices](https://www.youtube.com/watch?v=E8-e-3fRHBw)
+ [What Comes after Microservices?](https://www.youtube.com/watch?v=UDC3kwkBvkA)
+ [10 Tips for failing badly at Microservices by David Schmitz](https://www.youtube.com/watch?v=X0tjziAQfNQ)
+ [Neal Ford - Building Microservice Architectures](https://www.youtube.com/watch?v=pjN7CaGPFB4)
+ [Developing microservices with aggregates - Chris Richardson](https://www.youtube.com/watch?v=7kX3fs0pWwc)
+ [Martin Fowler – Microservices](https://www.youtube.com/watch?v=2yko4TbC8cI)
+ [Mastering Chaos - A Netflix Guide to Microservices]()



+ … law
  + design of organization will follow design of technology
  + MS therefore promotes few people directly responsible for their service and talking with customer
    + i.e. reputation service in Amazon
+ ESB - Enterprise Service Bus, SOA
  + have business logic in network orchestrating
  + services have very dump message-pipe only possible to deliver message to the provided address
+ conitnuous delivery
  + blue-green deployment
  + phoenix services
+ distributed objects
  + idea to treat RPC as local calls
  + wrong, local calls do not break
+ chaos-monkey
  + at netflix
  + a tool that randomly stop services
+ monoliths vs. micro-services
  + MS promotes using different storage, and data are always exchanded through service, never through database
  + RPC are additional complexity
  + micro-services are puting borders for refactoring
    + with monolitic code you can easier refactor
    + currently, successfull micro-services started as monolithic and then migrated to micro-services inccrementally
    + MS are supportinh modules easily
    + MS support different platforms and languages
+ necessary for successful MS
  + have servers provisioning fast (authomatic)
  + make support for monitoring
  + rapidly deployment of services in the provisioned servers
    + roll back quickly
      + old version of the service, if something is wrong
  + devops culture
    + this rises bar on operation-peple signifitcally

[Using sagas to maintain data consistency in a microservice architecture by Chris Richardson](https://www.youtube.com/watch?v=YPbGW3Fnmbc)

[An Overview of Designing Microservices - March 2017 AWS Online Tech Talks](https://www.youtube.com/watch?v=Ijs55IA8DIk)

[Principles Of Microservices by Sam Newman](https://www.youtube.com/watch?v=PFQnNFe27kU)

[What is Docker | Docker Tutorial for Beginners | Docker Container | DevOps Tools | Edureka](https://www.youtube.com/watch?v=lcQfQRDAMpQ)

+ ​

[GOTO 2016 • What I Wish I Had Known Before Scaling Uber to 1000 Services • Matt Ranney](https://www.youtube.com/watch?v=kb-m2fasdDY)

+ Heatmaps
+ any kind of representation on speed
+ a way to understand high-level picture
+ auto-generated and non-service specific dashboard
+ Tracing
  + Z… or OpenTracing

[Kubernetes in production - blue-green deployment, auto scaling and deployment automation](https://www.youtube.com/watch?v=-Ci4vd4rh4M)



# Clouds

## Nextcloud vs ownCloud

+ https://project-management.zone/system/nextcloud,owncloud
+ https://nextcloud.com/blog/3-reasons-to-upgrade-your-owncloud-instance-to-nextcloud-and-how-easy-it-is/
+ https://nextcloud.com/compare/
+ ​