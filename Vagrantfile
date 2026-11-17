
Vagrant.configure("2") do |config|

  config.vm.box = "ubuntu/jammy64"

  machines = [
    { name: "node1", ip: "192.168.56.22" },
    { name: "node2", ip: "192.168.56.23" },
    { name: "node3", ip: "192.168.56.24" }
  ]

  machines.each do |machine|

    config.vm.define machine[:name] do |node|

      node.vm.hostname = machine[:name]

      node.vm.network "private_network",
        ip: machine[:ip]

    end

  end

end
