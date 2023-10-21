# Swap Files

## Show existing swap config

```
sudo swapon --show
```

## Create a swap file

```
sudo fallocate -l 1G /swapfile
sudo chmod 600 /swapfile
sudo mkswap /swapfile
sudo swapon /swapfile
free -h
```

### Make perm

```
sudo cp /etc/fstab /etc/fstab.bak
echo '/swapfile none swap sw,pri=1 0 0' | sudo tee -a /etc/fstab
```

## Swappiness

60 for desktop
closer to 0 for server

```
cat /proc/sys/vm/swappiness
sudo sysctl vm.swappiness=20
sudo nano /etc/sysctl.conf
vm.swappiness=20
```

## Cache pressure setting

```
cat /proc/sys/vm/vfs_cache_pressure
sudo sysctl vm.vfs_cache_pressure=50
sudo nano /etc/sysctl.conf
vm.vfs_cache_pressure=50
```
