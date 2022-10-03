# Useful Commands

### Add User

```
adduser <username>
```

### Add user to group

```
usermod -aG <group> <user>
```

### Disable root account
Ensure a user has sudo ability and can sign into machine before running this
```
sudo passwd -l root
```
