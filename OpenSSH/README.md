# OpenSSH Server

OpenSSH is easy to install just run:

```
sudo apt-get install openssh-server
```

## Tips

### Configuration Suggestions
ssh configurations are located in `/etc/ssh/sshd_config`
- `PasswordAuthentication no` : a good idea to turn off Password authentication if you want to remotely access
- `Port 1234`: OpenSSH uses port 22 by default, change this port to weed out some unwanted accesses
- ```
    Match Address 10.0.0.0/24
            PasswordAuthentication yes
    ```
    - This allows password authentication on local devices
    - Notes: use `10.0.0.0/24` if your local ip is `10.0.0.X`, and `192.168.0.0/24` if it is `192.168.0.X`.
- Usually OpenSSH should start on boot by default, if you have issues some older solution ask you to run `sudo systemctl enable ssh.socket`, due to newer implementations `OpenSSH` no longer has as socket, so you should in fact try disabling `ssh.socket` (`sudo systemctl disable ssh.socket`)

### Access Suggestion
With password authentication turned off, your only way to authenticate is through public key. Create some RSA key pair if you haven't already (this is usually already done when you setup github). Place your remote machine's public key (`id_rsa.pub`) in server's authorized_keys file (`/home/<user_name>/.ssh/authorized_keys`). This will allow your remote machine to access your server.
- Note: You should never ever EVER share your private key `id_rsa`