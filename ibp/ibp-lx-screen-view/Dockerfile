FROM harbor.space.com/library/nginx:1.17-alpine
LABEL serverNmae: ops
ENV WORKSPACE=/opt
WORKDIR $WORKSPACE
COPY dist/ /tmp
EXPOSE 80
CMD ["sh", "-c", "sed -i \"s#<head>#<head> <meta id=ibp-api-config data-osms-gw-url=\"$OsmsGwUrl\"  data-psp-gw-url=\"$pspGwUrl\" data-ibp-gw-url=\"$ibpGwUrl\" data-iot-gw-url=\"$iotGwUrl\" data-auth-Weather-url=\"$authWeatherUrl\" data-dp-gw-url=\"$dpGwUrl\" data-env-Symbol=\"$envSymbol\"  /> #\" /tmp/index.html; if [[ -z ${pefixe} ]]; then  mv /tmp/* /opt/ ;else cp /tmp/index.html /opt/;mkdir /opt/\"$pefixe\"; mv /tmp/* /opt/\"$pefixe\";fi; nginx -g 'daemon off;'" ]