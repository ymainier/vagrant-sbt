# -*- mode: ruby -*-
# vi: set ft=ruby :
$install_a_jdk_and_sbt = <<SCRIPT
apt-get update
echo "Installing a 1.7 jdk"
apt-get install -y openjdk-7-jdk
echo "Installing sbt 0.12.4"
cd /opt/
curl -s -O http://scalasbt.artifactoryonline.com/scalasbt/sbt-native-packages/org/scala-sbt/sbt/0.12.4/sbt.tgz
tar xvzf sbt.tgz
echo "export PATH=/opt/sbt/bin:\$PATH" > /etc/profile.d/sbt.sh
SCRIPT

# Vagrantfile API/syntax version. Don't touch unless you know what you're doing!
VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  config.vm.box = "ubuntu/trusty64"
  config.vm.provider "virtualbox" do |v|
    v.memory = 2048
  end
  config.vm.provision "shell", inline: $install_a_jdk_and_sbt
end
