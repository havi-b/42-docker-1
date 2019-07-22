# **************************************************************************** #
#                                                                              #
#                                                         :::      ::::::::    #
#    Dockerfile                                         :+:      :+:    :+:    #
#                                                     +:+ +:+         +:+      #
#    By: hbhuiyan <marvin@42.fr>                    +#+  +:+       +#+         #
#                                                 +#+#+#+#+#+   +#+            #
#    Created: 2019/07/18 20:33:21 by hbhuiyan          #+#    #+#              #
#    Updated: 2019/07/18 20:33:23 by hbhuiyan         ###   ########.fr        #
#                                                                              #
# **************************************************************************** #

FROM alpine:latest

RUN apk update && \
	apk upgrade && \
	apk add vim

ENTRYPOINT vim

# Build Image
# docker build -t ex00 .

# Create Container
# docker run --name ex00 -it --rm ex00

