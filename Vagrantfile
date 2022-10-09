# -*- mode: ruby -*-
# vi: set ft=ruby :


Vagrant.configure("2") do |config|
  config.vm.box = "geerlingguy/centos7"
  config.vm.synced_folder ".", "/vagrant", disabled: true
  config.vm.provider :virtualbox do |v|
   v.memory = 512
   v.linked_clone = true 
  end
 
  ##ansible 
  config.vm.define "ansible" do |ans|
   ans.vm.hostname = "ansible-master"
   ans.vm.network :private_network , ip: "192.168.56.145"
  end
 ##webserver 
 config.vm.define "web" do |web|
   web.vm.hostname = "webserver"
   web.vm.network :private_network , ip: "192.168.56.146"
  end
 ##dbserver
 config.vm.define "db" do |db|
   db.vm.hostname = "dbserver"
   db.vm.network :private_network , ip: "192.168.56.147"
  end
 ##Appserver 1
 config.vm.define "app" do |app|
   app.vm.hostname = "appserver"
   app.vm.network :private_network , ip: "192.168.56.148"
  end
 
 
  
 end