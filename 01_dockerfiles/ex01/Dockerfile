# **************************************************************************** #
#                                                                              #
#                                                         :::      ::::::::    #
#    Dockerfile                                         :+:      :+:    :+:    #
#                                                     +:+ +:+         +:+      #
#    By: hbhuiyan <marvin@42.fr>                    +#+  +:+       +#+         #
#                                                 +#+#+#+#+#+   +#+            #
#    Created: 2019/07/18 20:33:38 by hbhuiyan          #+#    #+#              #
#    Updated: 2019/07/18 20:33:40 by hbhuiyan         ###   ########.fr        #
#                                                                              #
# **************************************************************************** #

FROM debian

ENV TS3SERVER_LICENSE=accept

EXPOSE 9987/udp 10011 30033

RUN apt-get update && \
	apt-get upgrade -y && \
	apt-get install -y wget bzip2 && \
	wget http://files.teamspeak-services.com/releases/server/3.9.1/teamspeak3-server_linux_amd64-3.9.1.tar.bz2 && \
	tar xvf teamspeak3-server_linux_amd64-3.9.1.tar.bz2

WORKDIR teamspeak3-server_linux_amd64

ENTRYPOINT  sh ts3server_minimal_runscript.sh

# Build Image
# docker build -t ex01 .

# Create Container
# docker run --name ex01 -it -p 9987:9987/udp -p 10011:10011 -p 30033:30033 ex01

