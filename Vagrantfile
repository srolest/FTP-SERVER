Vagrant.configure("2") do |config|
  
  # Servidor Anónimo
  config.vm.define "anonymous_server" do |anonymousserver|
    anonymousserver.vm.box = "generic/debian12"
    anonymousserver.vm.hostname = "anonymousserver"
    anonymousserver.vm.network "public_network", ip: "10.112.11.9", netmask: "255.255.0.0"
    
    anonymousserver.vm.provision "ansible" do |ansible|
      ansible.playbook = "playbook.yml"
      ansible.groups = {
        "anonymous_server" => ["anonymous_server"]
      }
    end
  end

  # Servidor Seguro
  config.vm.define "secure_server" do |secureserver|
    secureserver.vm.box = "generic/debian12"
    secureserver.vm.hostname = "secureserver"
    secureserver.vm.network "public_network", ip: "10.112.11.10", netmask: "255.255.0.0" 

    secureserver.vm.provision "ansible" do |ansible|
      ansible.playbook = "provision_secure.yml"
      ansible.groups = {
        "secure_server" => ["secure_server"]
      }
    end 
  end 
end