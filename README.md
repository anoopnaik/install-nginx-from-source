# Installing NGINX from source on Ubuntu 16.04 / CentOS 7

## Install NGINX Dependancies

###### Prior to compiling NGINX from the sources, it is necessary to install its dependencies:

###### Install development tools needed to build NGINX from source

> redhat base (CentOS):
> Before installing the Development tools, run the yum clean all command. This will clear the yum cache and force it to reread any changed configuration files.
```
yum clean all
yum groupinstall "Development tools"
```

> Debian base (Ubuntu):
```
apt-get install build-essential
```
  
  
###### the PCRE library – required by NGINX Core and Rewrite modules and provides support for regular expressions:
  - Check the latest version at ftp://ftp.csx.cam.ac.uk/pub/software/programming/pcre/ and change below code accordingly
```
cd /tmp/
wget ftp://ftp.csx.cam.ac.uk/pub/software/programming/pcre/pcre-8.39.tar.gz
tar -zxf pcre-8.39.tar.gz
cd pcre-8.39
./configure
make
sudo make install
```
  
###### the zlib library – required by NGINX Gzip module for headers compression:
  - Check the latest version at http://www.zlib.net and change below code accordingly
```
cd /tmp/
wget http://zlib.net/zlib-1.2.8.tar.gz
tar -zxf zlib-1.2.8.tar.gz
cd zlib-1.2.8
./configure
make
sudo make install
```
  
###### the OpenSSL library – required by NGINX SSL modules to support the HTTPS protocol:
  - Check the latest version at https://www.openssl.org/source/ and change below code accordingly
```
cd /tmp/
wget https://www.openssl.org/source/openssl-1.0.2h.tar.gz
tar -zxf openssl-1.0.2h.tar.gz
cd openssl-1.0.2h
./config
make
sudo make install
```
  
## Download and Install NGINX from source
  
###### Check the latest mainline version from http://nginx.org/en/download.html and change below code accordingly
```
cd /tmp/
wget http://nginx.org/download/nginx-1.11.3.tar.gz
tar -zxf nginx-1.11.3.tar.gz
cd nginx-1.11.3
./configure
make
sudo make install

```
