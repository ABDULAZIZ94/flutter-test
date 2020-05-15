# step zero
tar -xf archive.tar.xz
sudo update-alternatives --config java

# fluttertest

A new Flutter project.


# install flutter on ubuntu
# install jdk
sudo apt-get update && sudo apt install openjdk-8-jdk
# delete old jdk

# download flutter , extract then add it to env
wget https://storage.googleapis.com/flutter_infra/releases/stable/linux/flutter_linux_1.17.1-stable.tar.xz
tar xf ~/Downloads/flutter_linux_1.17.1-stable.tar.xz
export PATH="$PATH:`pwd`/flutter/bin" 
