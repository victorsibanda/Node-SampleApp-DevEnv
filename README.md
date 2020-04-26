# Node Sample App Dev AMI

This project consists of a Nodejs App and a Mongo Database.

- The repository contains a development environment for the project. It uses node package manager and provisioning of the app/db to display a working app, posts and fibonacci on a web browser.

- Implementation of a reverse proxy within the application in order to add security, performance and reliability.

### Prerequisites
- In order to for this project to run you must have the items below:

- Packer
- GIT
- Chef
- AWS Credentials
- AWS Key Pair
- Vagrant
- AWS CLI2
- VirtualBox

### Clone Repo
- Download this repository, open your terminal and run:
```
git clone git@github.com:victorsibanda/Node-SampleApp-DevEnv.git
```
### Testing
- Use VM
```
vagrant up

vagrant ssh app
```
- To Test the App
run:
```
cd /home/ubuntu/app

npm install
npm test

```

## Installation and Use
- In order to build an AMI using this repo

### Berksfile
- Download the relevant Cookbook files using
```
berks vendor Cookbooks
```

### Packer
- Validate the packer file using the command below:
```
packer validate packer.json
```
- If that is successful move on to the next step, although if any errors make the necessary edits.

- Now build your AMI Using:
```
packer build packer.json
```

- Once your AMI is Built, you may use it to create more instances. 
