Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/bionic64"
  config.vm.synced_folder "app/", "/var/www/app",
    create: true, group: "vagrant", owner: "vagrant",
    id: "app",
    type: "rsync", rsync__auto: true,
    disabled: false
end
