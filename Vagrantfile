Vagrant.configure("2") do |config|

    config.vm.define "web01" do |web01|
      web01.vm.box = "geerlingguy/ubuntu2004"
      web01.vm.network "private_network", ip: "192.168.62.13"
      web01.vm.provider "virtualbox" do |vb|
     end
     web01.vm.provision "shell", inline: <<-SHELL
        apt update
        apt install -y wget apache2 unzip -y
        systemctl start apache2
        systemctl enable apache2
        cd /tmp/
        wget https://www.tooplate.com/zip-templates/2108_dashboard.zip
        unzip -o 2108_dashboard.zip
        cp -r ./2108_dashboard/* /var/www/html
        systemctl restart apache2
       SHELL
      end
  
    config.vm.define "web02" do |web02|
      web02.vm.box = "geerlingguy/centos7"
      web02.vm.network "private_network", ip: "192.168.62.14"
      config.vm.provider "virtualbox" do |vb|
     end
     web02.vm.provision "shell", inline: <<-SHELL
        yum install wget httpd unzip -y
        systemctl start httpd
        systemctl enable httpd
        cd /tmp/
        wget https://www.tooplate.com/zip-templates/2121_wave_cafe.zip
        unzip -o 2121_wave_cafe.zip
        cp -r ./2121_wave_cafe/* /var/www/html
        systemctl restart httpd
    SHELL
    end
  end