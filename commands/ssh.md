# SSH Setup

## New SSH Key

```
ssh-keygen -t rsa -b 4096 
```

## Create authorized_keys

```
cp ./.ssh/id_rsa.pub ./.ssh/authorized_keys
chmod 600 ./.ssh/authorized_keys
```
