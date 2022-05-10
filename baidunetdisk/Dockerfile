FROM jlesage/baseimage-gui:debian-11
# Install xterm.
RUN apt update\
&&apt install wget -y\
&&wget https://issuepcdn.baidupcs.com/issue/netdisk/LinuxGuanjia/4.3.0/baidunetdisk_4.3.0_amd64.deb\
&&apt install -y ./baidunetdisk_4.3.0_amd64.deb\
&&rm baidunetdisk_4.3.0_amd64.deb\
&&apt install libgbm1 libasound2 ttf-wqy-zenhei -y
# Copy the start script.
COPY startapp.sh /startapp.sh

# Set the name of the application.
ENV TZ=Asia/Shanghai UMASK=000 DISPLAY_WIDTH=1600 DISPLAY_HEIGHT=900 APP_NAME="baidunetdisk"
