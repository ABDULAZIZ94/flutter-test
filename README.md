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
    sudo mv flutter/ /usr/lib

# download android cmd, extract then add it to env

    wget https://dl.google.com/android/repository/sdk-tools-linux-4333796.zip
    unzip sdk-tools-linux-4333796.zip
    mkdir Android
    export PATH="$PATH:`pwd`/flutter/bin"

# download gradle , extract and add to env

    wget https://downloads.gradle-dn.com/distributions/gradle-5.6.2-bin.zip
    unzip gradle-5.6.2-bin.zip
    mkdir gradle
    mv gradle-5.6.2/ gradle/
    sudo mv gradle/ opt/

# setting up android env

    $ sdkmanager "system-images;android-29;google_apis;x86_64"
    $ sdkmanager "platforms;android-29"
    $ sdkmanager "platform-tools"
    $ sdkmanager "patcher;v4"
    $ sdkmanager "emulator"
    $ sdkmanager "build-tools;29.0.2"

# upgrading to enable web

    flutter channel beta
    flutter upgrade

    flutter config --enable-web

# install google chrome at cloud

    wget https://dl.google.com/linux/direct/google-chrome-stable_current_amd64.deb

    sudo apt install ./google-chrome-stable_current_amd64.deb

# enable all port run wihout root
# save configuration permanently    
    echo 'net.ipv4.ip_unprivileged_port_start=0' > /etc/sysctl.d/50-unprivileged-ports.conf
# apply conf
    sysctl --system

# run flutter 
    flutter run -d chrome --web-port 80
    flutter run -d web-server --web-hostname 0.0.0.0 --web-port 80