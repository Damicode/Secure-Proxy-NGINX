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
#setting up environment
ENV nginx /nginx-files
#create a directory location
RUN mkdir $nginx
#setting up the working directory
WORKDIR $nginx
# remove the default nginx.conf file
RUN rm /etc/nginx/nginx.conf

#confirmation of removal
RUN ls /etc/nginx
#check if the default.conf still there inside the conf.d
RUN ls /etc/nginx/conf.d/
# Now lets get the custom nginx.conf file localy and copy it to replace the nginx.conf file removed above
COPY nginx.conf  /etc/nginx
COPY nginx.conf /usr/share/nginx/html
#copy everything else to the current working directory
COPY . .
#RUN openssl dhparam -out /etc/ssl/certs/dhparam.pem 2048
#RUN ln -s /etc/nginx/sites-available/my_app_1  /etc/nginx/sites-.*


