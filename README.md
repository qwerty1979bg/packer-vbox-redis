# Packer template to create a vagrant box containing REDIS using VirtualBox

This repository contains a Packer template for building a vagrant box containing REDIS using VirtualBox

## Usage

1. [Install Packer](https://www.packer.io/intro/getting-started/install.html#precompiled-binaries)
2. [Install VirtualBox](https://www.virtualbox.org/manual/ch02.html)
3. [Install VirtualBox Extension Pack](https://www.virtualbox.org/manual/ch01.html#intro-installing)
4. Clone this repository and `cd` into it.

5. Run the following:

```
$ export VAGRANT_CLOUD_TOKEN=<Your ATLAS / Vagrant Cloud Token>
$ packer build redis64.json
```
6. "After testing, "release" the version in the [Vagrant Cloud website](https://app.vagrantup.com/)

At the end, you should have an OVF + VMDK and BOX files ready to use.
Also the BOX should be uploaded automagically to the Vagrant Cloud.

## To use the box with Vagrant:

```
$ vagrant init qwerty1979/redis64
$ vagrant up
```

## To use `kitchen` to check the build:

1. [Install Chef/Kitchen](https://kitchen.ci/docs/getting-started/installing/)
2. Run `kitchen test`
