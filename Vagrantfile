# -*- mode: ruby -*-
# vi: set ft=ruby :

# All Vagrant configuration is done below. The "2" in Vagrant.configure
# configures the configuration version (we support older styles for
# backwards compatibility). Please don't change it unless you know what
# you're doing.
Vagrant.configure("2") do |config|
  # The most common configuration options are documented and commented below.
  # For a complete reference, please see the online documentation at
  # https://docs.vagrantup.com.

  # Every Vagrant development environment requires a box. You can search for
  # boxes at https://vagrantcloud.com/search.
  config.vm.box = "ubuntu/bionic64"

  config.vm.provider "virtualbox" do |vb|
   # Display the VirtualBox GUI when booting the machine
   vb.gui = true
 end

 # https://askubuntu.com/questions/1067929/on-18-04-package-virtualbox-guest-utils-does-not-exist
 config.vm.provision "shell", inline: "sudo apt-add-repository multiverse && sudo apt-get update"

 # Install xfce and virtualbox additions.
 # (Not sure if these packages could be helpful as well: virtualbox-guest-utils-hwe virtualbox-guest-x11-hwe)
 config.vm.provision "shell", inline: "sudo apt-get install -y xfce4 virtualbox-guest-dkms virtualbox-guest-utils virtualbox-guest-x11"
 # Permit anyone to start the GUI
 config.vm.provision "shell", inline: "sudo sed -i 's/allowed_users=.*$/allowed_users=anybody/' /etc/X11/Xwrapper.config"

 # Optional: Use LightDM login screen (-> not required to run "startx")
 config.vm.provision "shell", inline: "sudo apt-get install -y lightdm lightdm-gtk-greeter"
 # Optional: Install a more feature-rich applications menu
 config.vm.provision "shell", inline: "sudo apt-get install -y xfce4-whiskermenu-plugin"
 #install tkinter 
 config.vm.provision "shell", inline: "sudo apt-get install -y python3-tk"
 #install pip
 config.vm.provision "shell", inline: "sudo apt-get install -y python3-pip"
 #install numpy
 config.vm.provision "shell", inline: "sudo pip3 install numpy"
 #install matplotlib
 config.vm.provision "shell", inline: "sudo pip3 install -U matplotlib"
end
