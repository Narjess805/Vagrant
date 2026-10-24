# vi: ft=ruby:ts=2:ai:sw=2
Vagrant.configure("2") do |config|
  config.vm.box = "bento/ubuntu-24.04"
  config.vm.hostname = "vagrant-web1"
  
  config.vm.network "forwarded_port", guest: 80, host: 8080, host_ip: "0.0.0.0"
  config.vm.synced_folder "web/", "/var/www/html"

  config.vm.provider "virtualbox" do |vb|
    vb.name = "vagrant-web1"
    vb.memory = 1024
    vb.cpus = 2
  end
end
