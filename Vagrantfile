Vagrant.configure("2") do |config|

    config.vm.define "ubuntu" do |u|
        u.vm.box = "ubuntu/xenial64"
        u.vm.hostname = "ubuntu"
        #u.vm.network "private_network", ip: "172.16.42.101"
        u.vm.network "public_network", bridge: "eno1"
        u.vm.provider "virtualbox" do |v|
            v.memory = 1024
            v.cpus = 1
        end
        u.vm.provision "docker" do |d|
          d.build_image "/vagrant/nodejs", args: "-t image_test"
          d.run "test", image: "image_test", args: "-p 8080:8080 --name test"

        end
    end

end
