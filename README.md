### PHP 7.1 dev vagrant machine

This is a small vagrant machine with php 7.1(including xdebug), mysql, and nginx.

Provisioning is done using ansible, so make sure to have it available on your system.

For user that have never used vagrant before(OSX only):
```bash
brew install caskroom/cask/virtualbox
brew install vagrant
brew install ansible
```

The ip of the vm, as defined in the Vagrantfile is: `192.168.55.166`

The vhost preconfigured for nginx is: `my-dev-box.com`

So unless you change it make sure to add `192.168.55.166 my-dev-box.com` to your `/etc/hosts` file.

The preinstalled database is mysql 5.7 and the default credentials are:
```
user: devbox
password: devbox
```

Xdebug is already cofigured to connect back to your host machine, so if you are using phpstorm make sure to enable the listening(port 9000, as default).