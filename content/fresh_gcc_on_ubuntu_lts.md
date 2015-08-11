Title: How to install fresh gcc on ubuntu precise
Date: 2015-08-11 17:25
Category: linux
Tags: linux, gcc, ubuntu, ppa, toolchain

sudo add-apt-repository ppa:ubuntu-toolchain-r/test
sudo apt-get update; sudo apt-get install gcc-4.8 g++-4.8

sudo update-alternatives --remove-all gcc
sudo update-alternatives --remove-all g++
sudo update-alternatives --install /usr/bin/gcc gcc /usr/bin/gcc-4.8 20
sudo update-alternatives --install /usr/bin/g++ g++ /usr/bin/g++-4.8 20
sudo update-alternatives --config gcc
sudo update-alternatives --config g++
