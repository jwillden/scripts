# Build Docker image for Raspbian OS

Download the latest raspbian OS image file *.img

`fdisk -l [image file name]`

You probably want the second parition

To mount image using loop device

`sudo losetup -Pr /dev/loop0 [image file name]
mkdir rpi
sudo mount -o ro /dev/loop0p2 ./rpi`

Create a tarball from the file system

`sudo tar -C ./rpi -czpf raspbian.gz --numeric-owner .`

To list the contents of the .gz

` tar --numeric-owner -tvzf raspbian.gz`

Unmount locations used in loop device
`sudo umount ./rpi
sudo losetup -d /dev/loop0`

Create a Dockerfile similar to the one in this repo

Build the Dockerfile

`docker build -t raspbian-image .`

All done! Run the docker image

`docker run -it raspbian-image`

Instructions copied from https://www.guoyiang.com/2016/11/04/Build-My-Own-Raspbian-Docker-Image/

