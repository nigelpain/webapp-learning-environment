Vagrant.configure(2) do |config|
  #Use the Land Registry's default Ubuntu image
  config.vm.box = "landregistry/ubuntu"
  #Run the provisioning script to install necessary apps and such
  config.vm.provision :shell, path: "bootstrap.sh"
  #Setup the synched folder on the Vagrant image
  config.vm.synced_folder "webapp-learning/", "/webapp-learning"
  #Setup port forwarding so that you can access the server
  config.vm.network :forwarded_port, host: 8011, guest: 5000
end
