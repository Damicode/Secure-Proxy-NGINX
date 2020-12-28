# your code goes here ...

# Use NGINX image

FROM nginx



#RUN groupdel  nginx 
# Create nginx user/group first, to be consistent throughout Docker variants
#RUN  groupadd  --gid 1000  nginx 
#RUN  useradd  --uid 1000 --gid nginx --shell /bin/bash --create-home  nginx

# Chown all the files to the app user.
RUN chown -R nginx:nginx  /etc/nginx/conf.d/*.conf 
RUN  chmod 777  /etc/nginx/conf.d

USER nginx

# Replace nginx.conf file with our own to the address mentioned 

RUN rm /etc/nginx/conf.d/default.conf

COPY nginx.conf  /etc/nginx/conf.d/
COPY nginx.conf /usr/share/nginx/html
#COPY conf /etc/nginx

CMD ["nginx", "-g", "daemon off;"]


