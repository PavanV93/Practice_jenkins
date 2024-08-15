after creations of jenkins instance in AWS
loging with using of public ip on superputty
after login to the instance got to root user using below command 
sudo su -
then install jenkins using of below commands 
wget -O /usr/share/keyrings/jenkins-keyring.asc \
  https://pkg.jenkins.io/debian-stable/jenkins.io-2023.key

if you get any eroor try with below commands to install jenkins 

cd /etc/yum.repos.d/
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
1. anyone can login and do the changes, diffcult to track what went wrong
2. diffcult to restore
3. i cant see the history, no versions

scripted way:
1. review can be done before do something
2. east to restore
3. track the changes
4. maintain the history

Jenkins is master node,

install agents and distributed the pipelines to the agents.

jenkins needs mandiatory nodes..

master and node architecture

1. when work is there, master calls agent and ask them to do work (push based architecture)

create jenkins node instance in aws
then install java with using above commands

go to manage jenkins in master jenkins console
select and click on nodes tab-->> click on new node

cd /var/lib/jenkins/ ==>> home folder of jenkins (whatever the happends on jenkins changes in this path you wil find it everything)


create one master jenkins and two agent nodes and intergrate with git.


