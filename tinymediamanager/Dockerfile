FROM jlesage/baseimage-gui:debian-11
# Install xterm.
ARG TMM_LINK=https://release.tinymediamanager.org/v4/dist/tmm_4.2.8_linux-amd64.tar.gz
RUN apt update\
&&apt install wget libmediainfo0v5 ttf-wqy-zenhei kdialog -y \
&&cd /opt\
&&wget https://release.tinymediamanager.org/v4/dist/tmm_4.2.8_linux-amd64.tar.gz -O -|tar zx\
&&chmod 777 -R tinyMediaManager
# Copy the start script.
COPY startapp.sh /startapp.sh
ENV TZ=Asia/Shanghai UMASK=000 DISPLAY_WIDTH=1600 DISPLAY_HEIGHT=900 APP_NAME="tinyMediaManager"
