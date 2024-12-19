Vagrant.configure("2") do |config|

# Define the first VM - Primary
config.vm.define "primary" do |primary|
primary.vm.box = "ubuntu/jammy64"

# Network configuration
primary.vm.network "private_network", ip: "192.168.0.10", virtualbox__intnet: "internal_network"

# Hardware resources
primary.vm.provider "virtualbox" do |vb|
vb.memory = "2048" # 2GB RAM
vb.cpus = 1        # 1 CPU
end
end

# Define the second VM - Backup
config.vm.define "backup" do |backup|
backup.vm.box = "ubuntu/jammy64"

# Network configuration
backup.vm.network "private_network", ip: "192.168.0.20", virtualbox__intnet: "internal_network"

# Hardware resources
backup.vm.provider "virtualbox" do |vb|
vb.memory = "2048" # 2GB RAM
vb.cpus = 1        # 1 CPU
end
end

# Define the third VM - Attacker VM
config.vm.define "attacker" do |attacker|
attacker.vm.box = "ubuntu/jammy64"

# Network configuration
attacker.vm.network "private_network", ip: "192.168.0.30", virtualbox__intnet: "internal_network"

# Hardware resources
attacker.vm.provider "virtualbox" do |vb|
vb.memory = "1024" # 1GB RAM
vb.cpus = 1        # 1 CPU
end
end

end