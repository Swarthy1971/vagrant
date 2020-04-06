Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/bionic64"
  config.vm.synced_folder "app/", "/var/www/app", type: "nfs",
    create: true, id: "app",
    nfs_export: true, nfs_udp: "udp", nfs_version: 3,
    disabled: false
  config.vm.network "private_network", type: "dhcp"
end
