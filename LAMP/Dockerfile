FROM mattrayner/lamp
MAINTAINER Matthew Rayner <matt@mattrayner.co.uk>
ENV REFRESHED_AT 2016-08-21

RUN add-apt-repository -y ppa:ondrej/php && \
  apt-key adv --keyserver keyserver.ubuntu.com --recv-keys 4F4EA0AAE5267A6C && \
  apt-get update && \
  apt-get -y upgrade && \
  apt-get -y install postfix && \
  apt-get -y autoremove
  
CMD ["/run.sh"]
