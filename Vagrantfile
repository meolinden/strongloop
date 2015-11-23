# encoding: utf-8
# -*- mode: ruby -*-
# vi: set ft=ruby :

require 'yaml'

Vagrant.require_version ">= 1.7.0"

VAGRANTFILE_API_VERSION = "2"

current_dir    = File.dirname(File.expand_path(__FILE__))
devs = YAML.load_file("#{current_dir}/vagrant.yml")

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|

    config.vm.box = "strongloop/node-trusty"
    config.vm.network "private_network", ip: devs['ip']['local']
    config.vm.hostname = devs["domain"]
    config.vm.synced_folder devs['folder']['local'], devs['folder']["server"]

end
