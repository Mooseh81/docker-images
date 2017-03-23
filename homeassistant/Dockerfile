FROM homeassistant/home-assistant:latest
LABEL org.freenas.interactive="false"                                         \
      org.freenas.version="1"                                                 \
      org.freenas.upgradeable="false"                                         \
      org.freenas.expose-ports-at-host="true"                                 \
      org.freenas.autostart="true"                                            \
      org.freenas.port-mappings="8123:8123/tcp"                               \
      org.freenas.volumes="[						                  \
          {								                        \
              \"name\": \"/root/.homeassistant \",					      \
              \"descr\": \"Home Assisant Config\"		                              \
          }                                                                  \
          ]"
