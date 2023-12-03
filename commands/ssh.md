# SSH Setup

## New SSH Key using RSA using 4096 bits

This is an older algorithm, use ed25519 for more up-to-date security and speed where possible

```
ssh-keygen -t rsa -b 4096 
```

-t ed25519 = updated algorithm

-a 150 = number of key derivation function rounds (the optimal value between 80 and 200) 

## Create authorized_keys

```
cp ./.ssh/id_rsa.pub ./.ssh/authorized_keys
chmod 600 ./.ssh/authorized_keys
```
