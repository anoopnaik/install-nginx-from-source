# Installing NGINX from source on Ubuntu 16.04 / CentOS 7

cd /tmp/

# Get the latest mainline version from http://nginx.org/en/download.html
wget http://nginx.org/download/nginx-1.11.3.tar.gz
tar -xzf nginx-1.11.3.tar.gz
cd nginx-1.11.3
./configure
make
sudo make install
