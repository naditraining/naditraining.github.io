### Week 1: DevOps Concepts & Git Version Control

- DevOps Overview, SDLC, Agile vs DevOps
    - Hello  
- CI/CD Basics, DevOps Lifecycle
- Git essentials: clone, branch, merge, pull request - Yet to prepare the content.
- **Hands-on**: Collaborate using Git & GitHub

### Week 2: Linux & Shell Scripting for DevOps

- Linux basics: navigation, permissions, processes - check topics to cover in linux page
- Shell scripting: loops, conditionals, functions
- **Hands-on**: Automate routine admin tasks with scripts

**ADD GIT & GITHUB here (**https://www.learnxops.com/git-advanced-rebase-cherry-pick-conflict-resolution/)

### Week 5: CI/CD with Jenkins

- Jenkins concepts, plugin setup
- Freestyle and pipeline jobs (declarative syntax)
- **Hands-on**: Auto build and deploy from Git

### Week 6: Docker & Containerization

- docker basics
    - [**What is Containerization?](https://docs.docker.com/get-started/docker-concepts/the-basics/what-is-a-container/?_bhlid=2dd00407bd184499e60a572c566d23b12b0010ba&ref=learnxops.com)** – How containers differ from virtual machines and why they are beneficial.
    - [**Docker Terminology**](https://docs.docker.com/contribute/style/terminology/?_bhlid=7082ac9c069a4de99cd8d686ba46198933695b49&ref=learnxops.com)– Image (template), Container (running instance), Dockerfile, Docker Hub (image registry).
        - by default it uses the registry [docker.io](http://docker.io) which points to https://hub.docker.com/
        - you can mention customer registry while pulling images or docker file.
            
            ```
            docker pull [myregistry.example.com/myimage:tag](http://myregistry.example.com/myimage:tag)
            docker push [myregistry.example.com/myimage:tag](http://myregistry.example.com/myimage:tag)
            ```
            
        - note you need to login to custom registry using
        
        ```
        docker login myregistry.example.com
        
        ```
        
        - in k8s, they create item called secrets (custom registry details, username and password) and refer them in deployment file using parameter called imagePullSecrets.
        - in dockerfile, there is no direct login option, instead it uses the credentials saved in below path when building and pushing the image.
        
        ~/.docker/config.json
        
        - In jenkins, credentials stored in secrets or environment variables, and docker login will be performed before building and pushing image.
    - [**Docker Architecture**](https://docs.docker.com/get-started/docker-overview/?_bhlid=1cccc5fb496f6d1ee23945533584d23053c9cfb7&ref=learnxops.com#docker-architecture)– Understanding the client-server model, Docker Engine, and Docker Daemon.
        
        
        `Docker CLI
        ↓
        Docker Engine (dockerd)
        ↓
        containerd (manages lifecycle of containers)
        ↓
        runc (low-level runtime that does the actual Linux container isolation using namespaces and cgroups)`
        
    - [**Working with Containers](https://docs.docker.com/reference/cli/docker/container/?_bhlid=d570e704b906d49461ff1e5630d8a2782a37a592&ref=learnxops.com)** – Running, stopping, removing containers, mapping ports.
        - 
        
        [docker basic comands](https://www.notion.so/docker-basic-comands-20d8cbc78f5880a094fefd9bda809362?pvs=21)
        
    - [**Building Docker Images](https://docs.docker.com/get-started/docker-concepts/building-images/?_bhlid=aaa12433e8aaf7b08111fb77ddd0484bef8c8c92&ref=learnxops.com)** – Writing Dockerfile, adding dependencies, and optimizing images.
        - 
        
        [how to write dockerfile](https://www.notion.so/how-to-write-dockerfile-20e8cbc78f588071af1ff00b19015e19?pvs=21)
        
- Docker networking, volumes and compose
    - Docker Networking – Different network types (bridge, host, overlay), container communication, and linking containers.
    - Docker Volumes – Using volumes and bind mounts to persist data inside containers.
    - Docker Compose – Managing multi-container applications with docker-compose.yml.
    - Port Mapping & Exposing Services – Connecting applications running in different containers.
    - Persistent Storage – Ensuring database and application data survive container restarts.
    Service Scaling – Running multiple replicas of a service using Compose.
- Building and Running multi arch docker containers
- Tips to build production ready docker containers
- hands on docker projects

### Week 7: Kubernetes Fundamentals

- Kubernetes architecture, objects (Pods, Deployments, Services)
- Minikube or k3s setup
- **Hands-on**: Deploy Docker app in Kubernetes cluster

ADD GITOPS here

### Week 4: AWS Cloud Basics

- EC2, IAM, Key Pairs, Security Groups
- S3 introduction, AWS CLI
- **Hands-on**: Launch & connect to EC2, deploy an app

### Week 3: Configuration Management with Ansible

- YAML basics, inventory, modules
- Playbooks, roles, variables, handlers
- **Hands-on**: Provision a web server using Ansible

### Add Terraform here

Add GitOps too

Add Secrets management (Vault) 

### Week 8: Final Project + Terraform Basics + Career Prep

- Mini project: Git ➞ Jenkins ➞ Docker ➞ K8s CI/CD flow
- Terraform overview: launch EC2 with Terraform
- Resume building, GitHub project setup, interview Q&A
