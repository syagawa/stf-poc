PoC for STF deployment on a vagrant

---

# Installation

1. Install Virtualbox and Vagrant to PC.
2. Create a new directory on PC.
    * ex. C:\vagrant\sample
    * ex. /vagrant/sample
3. Copy Vagrantfile of this repository in a new directory.
4. Edit "change me" in Vagrantfile
5. in new directory
  * `$ vagrant up`
  * `$ vagrant ssh`
6. install docker
7. install docker-compose
8. clone this repository

# Usage

choose an IP your deployment should use, usually that will be the IP of your host.
choose a secret to be used for inter-service authentication.
Update the `.env` file accordingly.

* ex. PUBLIC_IP: your pc ip
* ex. WEB_PORT: your PC port


Run `docker-compose up -d --build`  
Point your browser to the IP you chose,  
login by providing any username and valid e-mail.


A little write-up on this setup:  
https://medium.com/@nikosch86/getting-started-with-automated-in-house-testing-on-android-smartphones-using-stf-dafecee4a8ee  
If you clap it will make me happy :)
