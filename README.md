# dearfad.com
Files for dearfad.com

```sh

# Add User
useradd -m dearfad
passwd dearfad
vim /etc/sudoers

# Install Docker for CentOS 7.6

curl -fsSL https://get.docker.com -o get-docker.sh
sudo sh get-docker.sh

# Install Docker for Aliyun Linux 2.1903

sudo yum install -y yum-utils device-mapper-persistent-data lvm2
sudo yum-config-manager --add-repo https://download.docker.com/linux/centos/docker-ce.repo
sudo yum install docker-ce docker-ce-cli containerd.io

# Use Docker as a non-root user

sudo usermod -aG docker $USER

# Log out and log back for group membership re-evaluated

logout

# Configure Docker to start on boot
sudo systemctl enable docker
sudo systemctl start docker

# Start httpd Service
docker run -d --name httpd -p 80:80 dearfad/dearfad.com

# Start Protainer

# Start Moon Predictor

# Start OpenVPN

# Start mmhelper Service
docker run -d --name mmhelper --restart=always -p 8888:8888 dearfad/mmhelper start.sh jupyter notebook --NotebookApp.token=''

# Start mrhelper Service
sudo yum install xorg-x11-xauth
sudo yum install bzip2
wget https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh
sudo sh Miniconda3-latest-Linux-x86_64.sh
cd ~/miniconda3
conda init
mkdir ~/.pip
vim ~/.pip/pip.conf
[global]
trusted-host=mirrors.aliyun.com
index-url=https://mirrors.aliyun.com/pypi/simple/

```
