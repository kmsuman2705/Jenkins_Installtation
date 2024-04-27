# jenkinsinstalltation
# Setup Instructions

## Installing Java

To install Java 17 on Linux, you can use the following script:

```bash
cd ~
wget --no-cookies --no-check-certificate --header "Cookie: gpw_e24=http%3A%2F%2Fwww.oracle.com%2F; oraclelicense=accept-securebackup-cookie" "https://download.oracle.com/java/17/latest/jdk-17_linux-x64_bin.rpm"
sudo rpm -ivh jdk-17_linux-x64_bin.rpm
sudo yum update
sudo wget -O /etc/yum.repos.d/jenkins.repo https://pkg.jenkins.io/redhat-stable/jenkins.repo
sudo rpm --import https://pkg.jenkins.io/redhat-stable/jenkins.io-2023.key
sudo yum upgrade
yum install fontconfig java-17-openjdk -y
sudo amazon-linux-extras install java-openjdk11 -y
sudo yum install jenkins -y
sudo systemctl enable jenkins
sudo systemctl start jenkins
