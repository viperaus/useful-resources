Alpine container setup for nested docker containers

```
# update apk cache and install latest updates
apk update
apk upgrade

# install additional tools
apk add nano htop sudo

# add new user and add to sudo
adduser <username>
adduser <username> wheel

# edit sudoers file to ensure wheel group is allowed to run sudo
nano /etc/sudoers

#  Find this section and uncomment as instructed
## Uncomment to allow members of group wheel to execute any command
# %wheel ALL=(ALL:ALL) ALL

# verify user is able to run sudo commands
su <username>
sudo whoami

# lock root account
sudo passwd -l root

# details from: https://wiki.alpinelinux.org/wiki/Docker
# install docker and docker compose
sudo apk add docker docker-cli-compose

# set to run on startup (docker as root)
rc-update add docker default
service docker start
sudo addgroup <username> docker



```
