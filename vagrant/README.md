# vagrant

## version
$ vagrant version
Installed Version: 2.0.4
Latest Version: 2.0.4

You're running an up-to-date version of Vagrant!

## use ubuntu
$ vagrant box add ubuntu/xenial64
==> box: Loading metadata for box 'ubuntu/xenial64'
    box: URL: https://vagrantcloud.com/ubuntu/xenial64
==> box: Adding box 'ubuntu/xenial64' (v20180427.0.0) for provider: virtualbox
    box: Downloading: https://vagrantcloud.com/ubuntu/boxes/xenial64/versions/20180427.0.0/providers/virtualbox.box
    box: Download redirected to host: cloud-images.ubuntu.com
    box:
==> box: Successfully added box 'ubuntu/xenial64' (v20180427.0.0) for 'virtualbox'!

## prepare vagrantfile
Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/xenial64"
end

## start
$ vagrant up
Bringing machine 'default' up with 'virtualbox' provider...
==> default: Importing base box 'ubuntu/xenial64'...
　　　・
　　　・
　　　・
    default: VirtualBox Version: 5.2
==> default: Mounting shared folders...
    default: /vagrant => C:/Users/fan_t/work/github.com/sky0621/study-hc-tools/vagrant

## status
$ vagrant status
Current machine states:

default                   running (virtualbox)

The VM is running. To stop this VM, you can run `vagrant halt` to
shut it down forcefully, or you can run `vagrant suspend` to simply
suspend the virtual machine. In either case, to restart it again,
simply run `vagrant up`.

## login
$ vagrant ssh
Welcome to Ubuntu 16.04.4 LTS (GNU/Linux 4.4.0-122-generic x86_64)

 * Documentation:  https://help.ubuntu.com
 * Management:     https://landscape.canonical.com
 * Support:        https://ubuntu.com/advantage

  Get cloud support with Ubuntu Advantage Cloud Guest:
    http://www.ubuntu.com/business/services/cloud

0 packages can be updated.
0 updates are security updates.


vagrant@ubuntu-xenial:~$

## status
$ vagrant global-status
id       name    provider   state   directory
--------------------------------------------------------------------------------------------------
ec9d8e1  default virtualbox running C:/Users/fan_t/work/github.com/sky0621/study-hc-tools/vagrant

The above shows information about all known Vagrant environments
on this machine. This data is cached and may not be completely
up-to-date. To interact with any of the machines, you can go to
that directory and run Vagrant, or you can use the ID directly
with Vagrant commands from any directory. For example:
"vagrant destroy 1a2b3c4d"

## destroy
$ vagrant destroy 89716ed
    default: Are you sure you want to destroy the 'default' VM? [y/N] y
==> default: Forcing shutdown of VM...
==> default: Destroying VM and associated drives...

## ssh-config
$ vagrant ssh-config
Host default
  HostName 127.0.0.1
  User vagrant
  Port 2222
  UserKnownHostsFile /dev/null
  StrictHostKeyChecking no
  PasswordAuthentication no
  IdentityFile C:/Users/fan_t/work/github.com/sky0621/study-hc-tools/vagrant/.vagrant/machines/default/virtualbox/private_key
  IdentitiesOnly yes
  LogLevel FATAL
