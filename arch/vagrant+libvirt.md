* if we get "out of memory" error in virNetworkCreate, we need sudo pacman -S ebtables: https://bbs.archlinux.org/viewtopic.php?id=191612. We also need bridge-utils, but that error message is more helpful
* Install vagrant-kvm: https://github.com/adrahon/vagrant-kvm/wiki/Install_on_ArchLinux WHOEVER, do NOT use the modified `CONFIGURE_ARGS` around `vagrant plugin install vagrant-kvm`: https://github.com/adrahon/vagrant-kvm/issues/161#issuecomment-38834996
* Install vagrant-libvirt: see vagrant-kvm installation. Also don't use `CONFIGURE_ARGS` like mistakenly described here: https://wiki.archlinux.org/index.php/Vagrant#vagrant-libvirt
* Don't use both plugins at the same time, they share namespaces for some
  reason...
