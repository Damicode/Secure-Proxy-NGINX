# Use NGINX image

FROM nginx

# Create nginx user/group first, to be consistent throughout Docker variants
#RUN  groupadd  --gid 1005  nginx
#RUN  useradd  --uid 1005 --gid nginx --shell /bin/bash --create-home nginx

# Change ownership to all the files to the app user.

#RUN useradd -ms /bin/bash nginx -f
#RUN chown -R :nginx  /etc/nginx/conf.d/*.conf

# addding nginx to the group nginx
#RUN usermod -aG nginx1 nginx1

#RUN ls -lah /var/log/nginx
#RUN ls -lah /etc/nginx/conf.d
#RUN ls -lah /etc/nginx/conf.d/nginx.conf
#EXPOSE 80
RUN whoami; id

ENV nginx /nginx-files
RUN mkdir $nginx
WORKDIR $nginx
# Replace nginx.conf file localy to the container remotely 
RUN cat /etc/nginx/conf.d/default.conf
RUN ls /etc/security
COPY nofile.conf /etc/security/limits.d
RUN cat /etc/security/limits.d/nofile.conf
RUN ls /etc/security/limits.d
RUN ls /etc/nginx/conf.d
RUN rm /etc/nginx/nginx.conf


RUN ls /etc/nginx

RUN ls /etc/nginx/conf.d/

COPY nginx.conf  /etc/nginx
COPY nginx.conf /usr/share/nginx/html
COPY . .
#RUN openssl dhparam -out /etc/ssl/certs/dhparam.pem 2048
#RUN ln -s /etc/nginx/sites-available/my_app_1  /etc/nginx/sites-.*
RUN pwd
RUN ls
RUN ls /nginx-files/files

