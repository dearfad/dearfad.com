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

# Use Docker as a non-root user
sudo usermod -aG docker $USER

# Configure Docker to start on boot
sudo systemctl enable docker
sudo systemctl start docker

# Start httpd Service
docker run -d --name httpd -p 80:80 dearfad/dearfad.com

# Start mmhelper Service
docker run -d --name mmhelper --restart=always -p 8888:8888 dearfad/mmhelper start.sh jupyter notebook --NotebookApp.token=''

# Start mrhelper Service
sudo yum install xorg-x11-xauth

```
