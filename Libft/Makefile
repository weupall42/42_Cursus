# **************************************************************************** #
#                                                                              #
#                                                         :::      ::::::::    #
#    Makefile                                           :+:      :+:    :+:    #
#                                                     +:+ +:+         +:+      #
#    By: sshin <marvin@42.fr>                       +#+  +:+       +#+         #
#                                                 +#+#+#+#+#+   +#+            #
#    Created: 2021/05/04 11:31:11 by sshin             #+#    #+#              #
#    Updated: 2021/05/04 15:20:16 by sshin            ###   ########.fr        #
#                                                                              #
# **************************************************************************** #

NAME = libft.a
CC = gcc
CFLAGS = -c -Wall -Wextra -Werror

HEADER = libft.h

BONUS_SCRS = $(wildcard *lst*.c)
BONUS_OBJS = $(BONUS_SRCS:.c=.o)

SRCS = $(filter-out $(BONUS_SRCS), $(wildcard *.c))
OBJS = $(SRCS:.c=.o)

all: $(NAME)

$(NAME): $(OBJS)
	ar -cr $@ $^

bonus: $(BONUS_OBJS) $(OBJS)
	ar -cr $(NAME) $^

%.o: %.c $(HEADER)
	$(CC) $(CFLAGS) $< -o $@

clean:
	rm -f $(OBJS) $(BONUS_OBJS)

fclean: clean
	rm -f $(NAME)

re: fclean all