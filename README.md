# kali-docker

a docker container running a customizable full Kali Linux distribution.

The build script lets you chose

- which remote access software you want to use (vnc, x2go, rdp)
- which network you want to use  (host, bridge)
- which Kali Packages to install (core, default everything and so on)
- which Desktop environment to use ( xfce, kde, gnome, mate etc.)

## how to build

Download all the files into a subdirectory on your linux docker host, e.g. /home/marc/kali docker
then cd into that directory and run

    sudo ./build

The build script then asks you for all the options and builds the image, creates the container
and starts it. So in a nutshell, the complete command sequence in a linux shell to install on a Debian or Ubuntu Linux would be:

    apt update
    apt install git
    git clone https://github.com/k4m4rTaj/kali-docker.git
    cd kali-docker
    sudo ./build

## how to use

You can now connect to the container by launching your favourite remote access software. The default ports defined in the script are as follows:

- RDP on port 13389
- ssh / x2goserver on port 20022
- vnc on port 5908 / display :8

All user names are `kaliuser` and all passwords are `k4m4rTaj`

## more info

Find all details on [my youtube channel](https://www.youtube.com/k4m4rTaj)

You may also want to join [THE k4m4rTaj DISCORD SERVER](https://discord.com/invite/DXnfBUG) and chat life with me and/or others - cu there ;-)

docker run -tid --name kali_k4 --network bridge -p 13389:13389 -v /Users/daniel/kali/home/kaliuser:/home/kaliuser k4m4rtaj/kali:latest
