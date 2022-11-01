FROM nginx:1.21.4 as geoiplib

FROM apache/apisix:2.15.0-debian

RUN apt-get update \
 && apt-get install -y libgeoip1

COPY --from=geoiplib /usr/lib/nginx/modules/ngx_http_geoip_module.so /usr/local/apisix/modules/ngx_http_geoip_module.so
