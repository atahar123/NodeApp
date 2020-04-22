# Node AMI

With this repo, you can make an AMI using Packer and this image can be used to create EC2 instances that have the app installed and setup, ready to be used with a database.


## What is Packer
Simply put, it's an open source tool maintained by Hashicorp which allows you to create duplicate machine images using just a single source file. This directory contains a file called packer.json which is used for that purpose. In this case, the Packer was created using Chef. It's a config management tool that provisions packages onto your machine.

## How to use
To begin clone the repository git clone:
```
git@github.com:atahar123/NodeApp.git
```

In Terminal, to clone the cookbooks:
```
berks vendor
```

To create the AMI, first validate by:
```
packer validate packer.json
```

Success with the above command? Run:
```
packer build packer.json
```
## Prerequisites
- AWS Access Key and ID

- Should be added as Environment variables into your .bashrc/.profile/.zshrc

- Variables should be named 'AWS_ACCESS_KEY_ID' and 'AWS_SECRET_ACCESS_KEY' to be used with the current packer.json

- Amazon key pair

- Packer

- Chef
