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