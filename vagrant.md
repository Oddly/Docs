# Vagrant
[Project GitHub](https://github.com/hashicorp/vagrant)
## Installation on RHEL/CentOS/Fedora
Install your virtualization platform:
- Install Libvirt
    - RHEL7/CentOS7: `$ yum install virt-manager libvirt libvirt-python virt-install`
    - Fedora30: `$ dnf install virt-manager libvirt libvirt-python`
- Install VirtualBox
    - RHEL7/CentOS7:
        ```sh
        $ wget -P /etc/yum.repos.d/ http://download.virtualbox.org/virtualbox/rpm/rhel/virtualbox.repo
        $ yum update && yum --enablerepo=epel install dkms kernel-devel && groupinstall "Development Tools"
        $ diff <(uname -r) <(rpm -qa kernel |sort -V |tail -n 1) && 
    - Fedora:
        ```
`$ wget -o https://releases.hashicorp.com/vagrant/2.2.4/vagrant_2.2.4_x86_64.rpm
$ yum install vagrant_2.2.4_86_64.rpm`

## Install Vagrant plugins

- **vagrant-libvirt:** Use the Libvirt provider. [Link](https://github.com/vagrant-libvirt/vagrant-libvirt)
- 

`$ vagrant plugin install vagrant-libvirt`

## Basic usage

**Command line:**

Usage: vagrant [options] <command> [<args>]

-v, --version                    Print the version and exit.
-h, --help                       Print this help.

Common commands:
**box:** manages boxes: installation, removal, etc.
**cloud:** manages everything related to Vagrant Cloud
**destroy:** stops and deletes all traces of the vagrant machine
**global-status:** outputs status Vagrant environments for this user
**halt:** stops the vagrant machine
**help:** shows the help for a subcommand
**init:** initializes a new Vagrant environment by creating a Vagrantfile
login
**package:** packages a running vagrant environment into a box
**plugin:** manages plugins: install, uninstall, update, etc.
**port:** displays information about guest port mappings
**powershell:** connects to machine via powershell remoting
**provision:** provisions the vagrant machine
**push:** deploys code in this environment to a configured destination
**rdp:** connects to machine via RDP
**reload:** restarts vagrant machine, loads new Vagrantfile configuration
**resume:** resume a suspended vagrant machine
**snapshot:** manages snapshots: saving, restoring, etc.
**ssh:** connects to machine via SSH
**ssh-config:** outputs OpenSSH valid configuration to connect to the machine
**status:** outputs status of the vagrant machine
**suspend:** suspends the machine
**up:** starts and provisions the vagrant environment
**upload:** upload to machine via communicator
**validate:** validates the Vagrantfile
**version:** prints current and latest Vagrant version
**winrm:** executes commands on a machine via WinRM
**winrm-config:** outputs WinRM configuration to connect to the machine

For help on any individual command run `vagrant COMMAND -h`

Additional subcommands are available, but are either more advanced
or not commonly used. To see all subcommands, run the command
`vagrant list-commands`.

## Examples
