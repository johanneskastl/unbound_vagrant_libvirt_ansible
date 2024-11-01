# unbound_vagrant_libvirt_ansible

This Vagrant setup creates a VM and installs a
[unbound](https://nlnetlabs.nl/projects/unbound/about/) instance on it.

Default OS is openSUSE Tumbleweed. Although that can be changed in the
Vagrantfile, please beware that this will break the Ansible provisioning.

There is a branch called `Leap_15.6` that uses openSUSE Leap 15.6.

## Vagrant

1. You need vagrant obviously. And ansible. And git...
1. Fetch the box, per default this is `opensuse/Leap-15.6.x86_64`, using
   `vagrant box add opensuse/Leap-15.6.x86_64`.
1. Make sure the git submodules are fully working by issuing `git submodule init
   && git submodule update`
1. Run `vagrant up`
1. Log in using `vagrant ssh` and try a DNS query using localhost:

  ```
  dig @127.0.0.1 opensuse.org
  ```

1. Party!

## Cleaning up

The VMs can be torn down after playing around using `vagrant destroy`.

## License

BSD-3-Clause

## Author Information

I am Johannes Kastl, reachable via git@johannes-kastl.de
