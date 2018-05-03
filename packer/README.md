# packer

## install
vagrant@ubuntu-xenial:~$ curl -o packer.zip https://releases.hashicorp.com/packer/1.2.3/packer_1.2.3_linux_amd64.zip
  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
100 17.8M  100 17.8M    0     0  6152k      0  0:00:02  0:00:02 --:--:-- 6152k
vagrant@ubuntu-xenial:~$
vagrant@ubuntu-xenial:~$ unzip packer.zip
Archive:  packer.zip
  inflating: packer
vagrant@ubuntu-xenial:~$
vagrant@ubuntu-xenial:~$ mv packer /bin/packer
vagrant@ubuntu-xenial:~$
vagrant@ubuntu-xenial:~$ packer version
Packer v1.2.3

