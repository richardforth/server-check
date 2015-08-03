# -*- mode: ruby -*-
# vi: set ft=ruby :

# Vagrantfile API/syntax version. Don't touch unless you know what you're doing!
VAGRANTFILE_API_VERSION = "2"

if !ENV['VAGRANT_OS']
  abort("VAGRANT_OS environment variable not specified. Supported values: 'debian', 'redhat', 'ubuntu'")
end

if ENV['VAGRANT_OS'].downcase == "redhat"
  box_name = "puppetlabs/centos-7.0-64-nocm"
elsif ENV['VAGRANT_OS'].downcase == "debian" || ENV['VAGRANT_OS'].downcase == "ubuntu"
  box_name = "puppetlabs/ubuntu-14.04-64-nocm"
else
  abort("VAGRANT_OS environment variable not specified. Supported values: 'debian', 'redhat', 'ubuntu'")
end

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  config.vm.box = box_name
  config.vm.network "private_network", ip: "192.168.33.10"
  # config.vm.provision "puppet" do |puppet|
  #   puppet.manifests_path = "manifests"
  #   puppet.manifest_file  = "site.pp"
  # end
end
