Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/bionic64"
  config.vm.synced_folder "app/", "/var/www/app",
    create: true, group: "vagrant", owner: "vagrant",
    id: "app",
    disabled: false
  config.vm.network "forwarded_port", guest: 8080, host: 8081,
    protocol: "tcp",
    auto_correct: true,
    id: "wanderer-app"
end
