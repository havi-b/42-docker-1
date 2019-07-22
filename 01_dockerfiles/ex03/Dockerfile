# **************************************************************************** #
#                                                                              #
#                                                         :::      ::::::::    #
#    Dockerfile                                         :+:      :+:    :+:    #
#                                                     +:+ +:+         +:+      #
#    By: hbhuiyan <marvin@42.fr>                    +#+  +:+       +#+         #
#                                                 +#+#+#+#+#+   +#+            #
#    Created: 2019/07/18 20:34:14 by hbhuiyan          #+#    #+#              #
#    Updated: 2019/07/21 16:27:46 by hbhuiyan         ###   ########.fr        #
#                                                                              #
# **************************************************************************** #

FROM ubuntu:18.04

RUN apt-get update && \
	apt-get upgrade -y && apt-get install -y dialog apt-utils && \
	apt-get install -y curl openssh-server ca-certificates postfix
	
RUN	curl https://packages.gitlab.com/install/repositories/gitlab/gitlab-ce/script.deb.sh | bash && \
	apt-get install -y gitlab-ce tzdata && \
	apt update && apt-get clean

EXPOSE 80 22 443

ENTRYPOINT (/opt/gitlab/embedded/bin/runsvdir-start &) && gitlab-ctl reconfigure && tail -f /dev/null

# Build Image
# docker build -t ex03 .

# Create Container
# docker run --name ex03 -it --rm -p 80:80 -p 22:22 -p 443:443 --privileged ex03

