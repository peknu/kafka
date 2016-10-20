Test Kafka:

https://objectpartners.com/2014/05/06/setting-up-your-own-apache-kafka-cluster-with-vagrant-step-by-step/
https://github.com/JGailor/vagrant-ansible-kafka
https://github.com/lloydmeta/ansible-kafka-cluster
https://allthingshadoop.com/2013/12/07/using-vagrant-to-get-up-and-running-with-apache-kafka/

Aim: Set up two "Hello World" like microservices that can communicate using a Kafka cluster (2-3 nodes)

Setup: Use Ansible, Vagrant & VirtualBox to set up the environment. Version manage with github
Create a java project with two spring boot modules, that should commúnicate with each other

1) Set up the cluster using Ansible and vagrant
2) Install Java on all nodes
3) Install ZooKeeper for the cluster (SBT?)
4) Install Apache Kafka on the cluster
5) Test the installation using the console producer/consumer
6) Install Java "Hello World" Applications
7) Configure connunicayion channels for the Java applications
8) Test how configuration works for topics, queues etc
9) Document conclutions

==============================================================================================================
vagrant init centos-7-user-modified

Fix SSH access:
https://github.com/mitchellh/vagrant/issues/7610
File: C:\HashiCorp\Vagrant\embedded\gems\gems\vagrant-1.8.5\plugins\guests\linux\cap\public_key.rb
Line 57: chmod 0600 ~/.ssh/authorized_keys
Fixed in next version of Vagrant (1.8.7): https://github.com/mitchellh/vagrant/blob/master/CHANGELOG.md

Test access to the box using Python HTTP server:
Vagrantfile: config.vm.network "forwarded_port", guest: 8000, host: 8000
cd /vagrant
python -m SimpleHTTPServer 8000

http://192.168.33.10:8000/

Install SBT using ansible: https://github.com/AnsibleShipyard/ansible-sbt/
https://github.com/glynnbird/ansible-install-kafka/blob/master/install-kafka-playbook.yml

Testing ZooKeeper (https://zookeeper.apache.org/doc/r3.3.3/zookeeperStarted.html#sc_ConnectingToZooKeeper)
cd /usr/local/zookeeper
./bin/zkCli.sh -server 127.0.0.1:2181
help