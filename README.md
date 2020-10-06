# Vagrant

```sh
$ vagrant --version
Vagrant 2.2.10
```

# Ansible

```sh
$ vagrant up dev
$ vagrant ssh dev
Welcome to Ubuntu 16.04.7 LTS (GNU/Linux 4.4.0-190-generic x86_64)
# .....
vagrant@ubuntu-xenial:~$ ansible --version
ansible 2.9.14
  config file = /etc/ansible/ansible.cfg
  configured module search path = [u'/home/vagrant/.ansible/plugins/modules', u'/usr/share/ansible/plugins/modules']
  ansible python module location = /usr/lib/python2.7/dist-packages/ansible
  executable location = /usr/bin/ansible
  python version = 2.7.12 (default, Jul 21 2020, 15:19:50) [GCC 5.4.0 20160609]
```

# Docker

Build Tests
-----------

```bash
sudo docker build -t vfarcic/books-ms-tests -f Dockerfile.test .
    
sudo docker push vfarcic/books-ms-tests
```

Test and Build
--------------

```bash
sudo docker-compose -f docker-compose-dev.yml run testsLocal

sudo docker build -t vfarcic/books-ms .

sudo docker push vfarcic/books-ms
```

Run Front-End Tests Watcher
---------------------------

```bash
sudo docker-compose -f docker-compose-dev.yml up feTests
```

Run Integration Tests
---------------------

```bash
sudo docker-compose -f docker-compose-dev.yml up integ
```

