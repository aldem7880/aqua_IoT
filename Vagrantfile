# -*- mode: ruby -*-
# vi: set ft=ruby :

VAGRANTFILE_API_VERSION = "2"
ENV['VAGRANT_DEFAULT_PROVIDER'] = 'virtualbox'

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
config.vm.define "iot" do |iot|
  iot.vm.hostname = "iot"
  iot.vm.network "private_network", ip: "192.168.22.94"
  iot.vm.box = "ubuntu/trusty64"
  iot.vm.box_url = "https://oss-binaries.phusionpassenger.com/vagrant/boxes/latest/ubuntu-16.04-amd64-vbox.box"
end

end
