# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/xenial64"
   config.vm.provision "shell", inline: <<-SHELL
     apt-get update
     sudo apt-get install -y git-core
     sudo apt-get install -y build-essential patch ruby-dev zlib1g-dev liblzma-dev
     sudo apt-get install nodejs
     git clone https://github.com/10bytes/indix.github.io.git
     cd indix*
     sudo gem install bundler
     bundle install
     bundle exec middleman serve
   SHELL
end
