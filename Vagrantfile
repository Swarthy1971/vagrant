Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/bionic64"


  config.vm.define "app" do |app|
    app.vm.hostname = "app"
    app.vm.synced_folder "app/", "/var/www/app",
      create: true, group: "vagrant", owner: "vagrant",
      id: "app",
      disabled: false
    app.vm.network "forwarded_port", guest: 8080, host: 8081,
      protocol: "tcp",
      auto_correct: true,
      id: "wanderer-app"
    app.vm.network "private_network", ip: "192.168.200.10"
  end
  config.vm.define "prom" do |prom|
    prom.vm.hostname = "prom"
    prom.vm.network "forwarded_port", guest: 9090, host: 9090,
      auto_correct: true, id: "prometeus"
    prom.vm.network "private_network", ip: "192.168.200.11"
  end
end
