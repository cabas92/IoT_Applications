# Starting RabbitMQ Over Debian (Raspberry) and Ubuntu

Check the next page for Raspberry:
https://www.iotshaman.com/blog/content/how-to-install-rabbitmq-on-a-raspberry-pi

## 1.) Install tools for RabbitMQ

  ### Erlang/OTP
  It's necessary for the operation of rabbitmq
  ```
  $ sudo apt-get update
  $ sudo apt-get install -y erlang logrotate
  $ sudo apt-get install
  ```
  or
  ```
  $ sudo apt-get update
  $ sudo apt-get install erlang-nox
  $ sudo apt-get install
  ```
  If you can, previously to the instalation upgrade the system.

  ### Python, pip and pika
  First install and check python3 or superior versión (I prefer Python 3.0)  
  ```
  $ sudo apt-get install python python3
  ```
  Next check for installation assistant fot python libraries pip and pip3
  ```
  $ sudo apt-get install python-pip python3-pip
  ```
  Finally, install pika toolbox to use AMQP message with python and RabbitMQ. This is the generic library for the examples and explenations.
  ```
  $ sudo pip3 install pika
  ```

## 2.) Install RabbitMQ

The are differents instalation methods but the most easy is with ubuntu repositories.
```
$ sudo apt-get install rabbitmq-server
```
more information:
https://www.rabbitmq.com/install-debian.html

## 3.) Check Server 

This process is automatic
```
$ sudo rabbitmq-server start
```

## 4.) Setup user 

Add user administrator and enable the management UI http interface:
```
$ sudo rabbitmq-plugins enable rabbitmq_management
$ sudo rabbitmqctl add_user [newuser] [password]
$ sudo rabbitmqctl set_user_tags [newuser] administrator
$ sudo rabbitmqctl set_permissions -p / [newuser] ".*" ".*" ".*"
```
__Restart the system__ for enable the http interface
Open the port **15672** in your IP with a web explorer, an adddress example: 192.168.0.12:15672
This is the web page for the configuration and monitoring of server RabbitMQ in your localhost, logging with your [newuser] and [password] previously defined.
### Aditional Setup
  - Delete guest user or change his password
  - Add new user for only puclish information

more information:
https://www.rabbitmq.com/rabbitmqctl.8.html
https://www.rabbitmq.com/access-control.html

## 5.) Check and start the examples

Each one of tutorials explain parts of the communications system based on ActiveMQ

more information:
https://www.rabbitmq.com/getstarted.html









