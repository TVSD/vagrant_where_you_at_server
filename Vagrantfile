# -*- mode: ruby -*-
# vi: set ft=ruby :

# Vagrantfile API/syntax version. Don't touch unless you know what you're doing!
VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  # Base Vagrant box which provides MongoDB & Node
  config.vm.box = "dansweeting/ubuntu-trusty64-mongo-node"

  # HTTP port for the NodeJS server defined by the where_you_at_server project
  config.vm.network "forwarded_port", guest: 1337, host: 1337

  # Specifices the mapped folder in the Vagrant VM.
  # The following expects that the "where_you_at_server" project is cloned into a
  #  sibling directory to the current directory for this Vagrantfile.
  config.vm.synced_folder "../where_you_at_server", "/server"

end
