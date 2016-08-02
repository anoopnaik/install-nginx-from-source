# Installing NGINX from source on Ubuntu 16.04 / CentOS 7

## Install NGINX Dependancies

###### Prior to compiling NGINX from the sources, it is necessary to install its dependencies:

###### Change to /tmp directory
```cd /tmp/```

###### the PCRE library – required by NGINX Core and Rewrite modules and provides support for regular expressions:
```
wget ftp://ftp.csx.cam.ac.uk/pub/software/programming/pcre/pcre-8.39.tar.gz
tar -zxf pcre-8.39.tar.gz
cd pcre-8.39
./configure
make
sudo make install
```
###### the zlib library – required by NGINX Gzip module for headers compression:
```
wget http://zlib.net/zlib-1.2.8.tar.gz
tar -zxf zlib-1.2.8.tar.gz
cd zlib-1.2.8
./configure
make
sudo make install
```

###### the OpenSSL library – required by NGINX SSL modules to support the HTTPS protocol:
```
wget http://www.openssl.org/source/openssl-1.0.2f.tar.gz
tar -zxf openssl-1.0.2f.tar.gz
cd openssl-1.0.2f
./configure darwin64-x86_64-cc --prefix=/usr
make
sudo make install
```

## Download and Install NGINX from Source

###### Get the latest mainline version from http://nginx.org/en/download.html and change below code accordingly
```
wget http://nginx.org/download/nginx-1.11.3.tar.gz
tar -zxf nginx-1.11.3.tar.gz
cd nginx-1.11.3
./configure
make
sudo make install

```

