after creations of jenkins instance in AWS
loging with using of public ip on superputty
after login to the instance got to root user using below command 
sudo su -
then install jenkins using of below commands 
wget -O /usr/share/keyrings/jenkins-keyring.asc \
  https://pkg.jenkins.io/debian-stable/jenkins.io-2023.key

if you get any eroor try with below commands to install jenkins 

cd /etc/tum.repos.d/
vim jenkins.repo
 inside the file add the below lines
[jenkins]
name=Jenkins-stable
baseurl=http://pkg.jenkins.io/redhat-stable
gpgcheck=1

then :wq! (save and quit)

next
rpm --import https://pkg.jenkins.io/redhat-stable/jenkins.io-2023.key
download the depencies like jave file reuired to run jenkins 
yum install fontconfig java-17-openjdk

yum install jenkins -y
systemctl daemon-reload

after installation to enable and start and staus the jenkins
sudo systemctl enable jenkins

sudo systemctl start jenkins

sudo systemctl status jenkins

copy the <public ip>:portnumber
go to google new tab give ex: 54.80.15.119:8080

page will reflect to jenkins page
then to get the admins password you will see the one path above of adminpassword copy that path and give like
cat <copy from jenkinspage>
ex: cat /var/lib/jenkins/secrets/initialAdminPassword

thenk click on installed suggested plugins
give the admin details with admin only
click start jenkins

pre build
build
post build

freestyle disadvantags:
1. anyone can login and do the changes, diffcult to track