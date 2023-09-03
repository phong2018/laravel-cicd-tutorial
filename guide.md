- check install java: java -version
- check docker: docker -v
- check docker compose: docker compose version
- install jenkins: https://www.digitalocean.com/community/tutorials/how-to-install-jenkins-on-ubuntu-22-04
- access jenkins: http://localhost:8080/ user: admin; pass: admin
- set permision for jenkins user: sudo usermod -aG docker jenkins
- create repository github for source code: Learning-jenkin-docker
- create credential for jenkin access respository in github
+ kind: SSH Username with private key
+ ID: github
+ username: phong2018
+ privatekey: select file
- cretae new job: domain/view/all/newJob
+ name: LaravelTest
+ type: pipeline
+ Definition: from pipeline script from scm
+ scm: git 
#####################################
- access ec2 by keypem
chmod 400 ec2_server_key_pair_app002.pem
ssh -i "ec2_server_key_pair_app002.pem" ec2-user@52.221.199.29
cat /etc/os-release

#####################################
- install httpd 
sudo yum update
sudo yum -y install httpd
sudo systemctl start httpd
sudo systemctl enable httpd
sudo systemctl status httpd  
sudo systemctl stop httpd
sudo nano /var/www/html/public/index.html
sudo chown ec2-user:ec2-user /var/www/html

#####################################
- install php9.0
sudo yum -y install https://dl.fedoraproject.org/pub/epel/epel-release-latest-7.noarch.rpm
sudo yum -y install https://rpms.remirepo.net/enterprise/remi-release-7.rpm
sudo yum -y install yum-utils
sudo yum-config-manager --disable 'remi-php*'
sudo yum-config-manager --enable remi-php80
sudo yum -y install php php-{cli,fpm,mysqlnd,zip,devel,gd,mbstring,curl,xml,pear,bcmath,json}
php --version
sudo amazon-linux-extras enable php8.0
#####################################
- create folder: mkdir /home/ec2-user/artifact
- cd /etc/httpd/conf: DocumentRoot "/var/www/html" -> DocumentRoot "/var/www/html/public"
#####################################
plugin: 
+ Pipeline Utility Steps
+ File Operations
+ SSH Agent