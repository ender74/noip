FROM armv7/armhf-ubuntu_core
MAINTAINER Heiko Hüter <ender@ender74.de> 

RUN apt-get update && apt-get -y install curl

VOLUME ["/config"]

# Add dynamic dns script 
ADD noip.sh /root/noip/noip.sh
RUN chmod +x /root/noip/noip.sh

# Create template config file 
ADD noip.conf /root/noip/noip.conf
CMD /root/noip/noip.sh

