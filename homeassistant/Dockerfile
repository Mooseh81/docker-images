FROM homeassistant/home-assistant:latest

RUN apt-get update
RUN curl -sL https://deb.nodesource.com/setup_8.x | bash -
RUN apt-get install -y nodejs
RUN npm install ps4-waker -g

LABEL org.freenas.interactive="false"                                         \
      org.freenas.version="1"                                                 \
      org.freenas.upgradeable="true"                                         \
      org.freenas.expose-ports-at-host="true"                                 \
      org.freenas.autostart="true"                                            \
      org.freenas.port-mappings="8123:8123/tcp"                               \
      org.freenas.volumes="[						                  \
          {								                        \
              \"name\": \"/root/.homeassistant \",					      \
              \"descr\": \"Home Assisant Config\"		                              \
          }                                                                  \
          ]"
