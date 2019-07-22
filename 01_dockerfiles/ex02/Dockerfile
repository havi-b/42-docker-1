# **************************************************************************** #
#                                                                              #
#                                                         :::      ::::::::    #
#    Dockerfile                                         :+:      :+:    :+:    #
#                                                     +:+ +:+         +:+      #
#    By: hbhuiyan <marvin@42.fr>                    +#+  +:+       +#+         #
#                                                 +#+#+#+#+#+   +#+            #
#    Created: 2019/07/18 20:33:52 by hbhuiyan          #+#    #+#              #
#    Updated: 2019/07/18 20:33:54 by hbhuiyan         ###   ########.fr        #
#                                                                              #
# **************************************************************************** #

FROM ft-rails:on-build

EXPOSE 3000

CMD ["rails", "s", "-b", "0.0.0.0", "-p", "3000"]

# Build Image
# docker build -t ex02 .

# Create Container
# docker run --name ex02 -it -p 3000:3000 ex02

