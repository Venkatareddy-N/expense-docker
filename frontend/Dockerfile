FROM nginx:mainline-alpine3.20-slim
RUN rm -rf /etc/nginx/nginx.conf && \
    rm -rf /etc/nginx/conf.d/default.conf 
COPY nginx.conf /etc/nginx/nginx.conf

COPY code /usr/share/nginx/html
