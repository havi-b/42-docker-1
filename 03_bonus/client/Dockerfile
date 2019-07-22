# **************************************************************************** #
#                                                                              #
#                                                         :::      ::::::::    #
#    Dockerfile                                         :+:      :+:    :+:    #
#                                                     +:+ +:+         +:+      #
#    By: hbhuiyan <hbhuiyan@student.42.fr>          +#+  +:+       +#+         #
#                                                 +#+#+#+#+#+   +#+            #
#    Created: 2019/07/18 20:37:42 by hbhuiyan          #+#    #+#              #
#    Updated: 2019/07/19 04:25:36 by hbhuiyan         ###   ########.fr        #
#                                                                              #
# **************************************************************************** #

FROM ubuntu:18.04

RUN apt update && apt upgrade -y && \
	apt install -y curl

RUN apt install -y npm && \
	curl -sS https://dl.yarnpkg.com/debian/pubkey.gpg | apt-key add - && \
	echo "deb https://dl.yarnpkg.com/debian/ stable main" | tee /etc/apt/sources.list.d/yarn.list

RUN apt update && apt upgrade -y && \
	apt install -y yarn git

RUN git clone https://github.com/havi-b/MERN-Shopping-List.git app

WORKDIR /app/client

WORKDIR /app/client/

RUN yarn

EXPOSE 3000

CMD ["yarn", "start"]
