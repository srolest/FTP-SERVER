Vagrant.configure("2") do |config|
  
  # Anonymous server
  config.vm.define "anonymous_server" do |anonymousserver|
    anonymousserver.vm.box = "generic/debian12"
    anonymousserver.vm.hostname = "anonymousserver"
    anonymousserver.vm.network "private_network", ip: "192.168.56.10" 
  end

  # Secure server
  config.vm.define "secure_server" do |secureserver|
    secureserver.vm.box = "generic/debian12"
    secureserver.vm.hostname = "secureserver"
    secureserver.vm.network "private_network", ip: "192.168.56.20" 
  end

end