# **************************************************************************** #
#                                                                              #
#                                                         :::      ::::::::    #
#    Dockerfile                                         :+:      :+:    :+:    #
#                                                     +:+ +:+         +:+      #
#    By: hbhuiyan <marvin@42.fr>                    +#+  +:+       +#+         #
#                                                 +#+#+#+#+#+   +#+            #
#    Created: 2019/07/18 18:44:35 by hbhuiyan          #+#    #+#              #
#    Updated: 2019/07/18 20:34:01 by hbhuiyan         ###   ########.fr        #
#                                                                              #
# **************************************************************************** #

FROM ruby:latest

RUN apt-get update && apt-get upgrade -y && \
	apt-get install -y nodejs && \
	gem install rails bundler

ONBUILD WORKDIR /opt
ONBUILD RUN rails new app

ONBUILD WORKDIR /opt/app
ONBUILD RUN bundle install
ONBUILD RUN rake db:migrate
ONBUILD RUN rake db:seed

# Build Image
# docker build -t ft-rails:on-build ft-rails

