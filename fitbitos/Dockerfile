# build stage
FROM ubuntu:bionic


# add 32bit arch.
RUN dpkg --add-architecture i386

ENV WINEARCH=win32

# install dependecies
RUN apt-get -qq update && apt-get install -y \
    wine32 \
    winetricks

# fitbit requires some different fonts
RUN winetricks -q corefonts

# Download fitbit OS
WORKDIR /fitbitos
RUN wget -O fitbitos.exe "https://simulator-updates.fitbit.com/Fitbit OS Simulator-latest-0.6.4.exe" 

ENTRYPOINT [ "/bin/bash" ]


