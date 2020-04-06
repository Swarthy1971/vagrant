Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/bionic64"
  config.vm.synced_folders "app/", "/var/www/app",
    create: true, group: "vagrant", owner: "vagrant",
    id: "app",
    disabled: false
end
