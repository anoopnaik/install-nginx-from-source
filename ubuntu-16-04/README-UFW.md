File: /etc/ufw/applications.d/nginx

Run:

To allow both HTTP and HTTPS protocols
ufw allow 'Nginx Full'

To allow HTTP only
ufw allow 'Nginx HTTP'

To allow HTTPS only
ufw allow 'Nginx HTTPS'
