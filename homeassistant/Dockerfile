FROM homeassistant/home-assistant:latest

RUN apt-get update && \
    apt-get install -y nodejs && \
    apt-get install -y telnet && \
    apt-get install -y libpcap-dev && \
    apt-get install -y git && \
    curl -sL https://deb.nodesource.com/setup_8.x | bash - && \
    npm install ps4-waker -g && \
    curl https://raw.githubusercontent.com/Mooseh81/home-assistant/master/dasherinit -o /etc/init.d/dasher && \
    chmod 755 /etc/init.d/dasher && \
    update-rc.d dasher defaults && \
    service dasher start && \
    systemctl enable dasher

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
