# dearfad.com
Files for dearfad.com

```sh

# Add User
useradd -m dearfad
passwd dearfad

# Install Docker for Ubuntu 18.04

curl -fsSL https://get.docker.com -o get-docker.sh
sudo sh get-docker.sh

# Use Docker as a non-root user
sudo usermod -aG docker $USER

# Configure Docker to start on boot
sudo systemctl enable docker

# Start Services
docker run -d --name dearfad.com -p 80:80 dearfad/dearfad.com
docker run -d --name mmhelper -p 8888:8888 dearfad/mmhelper start.sh jupyter notebook --NotebookApp.token=''

```