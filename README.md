
How To Install Jenkins & Terraform on Ubuntu 22.04

Jenkins:

sudo apt install openjdk-11-jre-headless -y

wget -q -O - https://pkg.jenkins.io/debian-stable/jenkins.io.key |sudo gpg --dearmor -o /usr/share/keyrings/jenkins.gpg

sudo sh -c 'echo deb [signed-by=/usr/share/keyrings/jenkins.gpg] http://pkg.jenkins.io/debian-stable binary/ > /etc/apt/sources.list.d/jenkins.list'

sudo apt update

sudo apt install jenkins

sudo systemctl start jenkins.service


Terraform:

apt update

wget https://releases.hashicorp.com/terraform/0.14.7/terraform_0.14.7_linux_amd64.zip

apt install unzip

unzip terraform_0.14.7_linux_amd64.zip

mv terraform /usr/local/bin/

terraform -v






Ansible,Jenkins, Docker & Terraform Installation:

Take amazon-linux-2 instance

yum update -y

sudo amazon-linux-extras install java-openjdk11 epel -y

sudo wget -O /etc/yum.repos.d/jenkins.repo https://pkg.jenkins.io/redhat/jenkins.repo

sudo rpm --import https://pkg.jenkins.io/redhat/jenkins.io-2023.key


sudo yum-config-manager --add-repo https://rpm.releases.hashicorp.com/AmazonLinux/hashicorp.repo

sudo yum install yum-utils awscli unzip maven git tree docker jenkins terraform ansible -y

sudo systemctl start docker

sudo systemctl enable docker

sudo systemctl start jenkins

sudo systemctl enable jenkins

Portnumber:

Jenkins 8080

RDP 3389

tomcat 8080

ssh - 22 

dns 53

sonar 9000

nexus 8081

sql 1433


wget -O- https://apt.releases.hashicorp.com/gpg | sudo gpg --dearmor -o /usr/share/keyrings/hashicorp-archive-keyring.gpg
echo "deb [signed-by=/usr/share/keyrings/hashicorp-archive-keyring.gpg] https://apt.releases.hashicorp.com $(lsb_release -cs) main" | sudo tee /etc/apt/sources.list.d/hashicorp.list

apt update 

apt install terraform -y

