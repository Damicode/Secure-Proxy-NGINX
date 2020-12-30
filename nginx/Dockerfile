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
EXPOSE 80
RUN whoami; id

# Replace nginx.conf file localy to the container remotely 

RUN rm /etc/nginx/conf.d/default.conf

COPY nginx.conf  /etc/nginx/conf.d/
COPY nginx.conf /usr/share/nginx/html


