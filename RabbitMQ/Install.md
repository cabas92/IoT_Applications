# Starting RabbitMQ Over Debian (Raspberry) and Ubuntu

Check the next page for Raspberry:
https://www.iotshaman.com/blog/content/how-to-install-rabbitmq-on-a-raspberry-pi

## 1.) Install tools for RabbitMQ

more information:
https://www.rabbitmq.com/install-debian.html

  ### Erlang/OTP
  It's necessary for the operation of rabbitmq
  ```
  sudo apt-get update
  sudo apt-get install -y erlang logrotate
  sudo apt-get install
  ```
  or
  ```
  sudo apt-get update
  sudo apt-get install erlang-nox
  sudo apt-get install
  ```
  If you can, previously to the instalation upgrade the system.

  ### Python, pip and pika
  First install and check python3 or superior versión (I prefer Python 3.0)  
  Next check for installation assistant fot python libraries pip and pip3
  
  


## 2.) Setup user 

more information:

https://www.rabbitmq.com/rabbitmqctl.8.html











