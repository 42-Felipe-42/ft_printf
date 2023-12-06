# **************************************************************************** #
#                                                                              #
#                                                         :::      ::::::::    #
#    Makefile                                           :+:      :+:    :+:    #
#                                                     +:+ +:+         +:+      #
#    By: plangloi <plangloi@student.42.fr>          +#+  +:+       +#+         #
#                                                 +#+#+#+#+#+   +#+            #
#    Created: 2023/11/20 14:02:16 by plangloi          #+#    #+#              #
#    Updated: 2023/11/30 10:35:05 by plangloi         ###   ########.fr        #
#                                                                              #
# **************************************************************************** #

NAME = libftprintf.a

CC = cc

RED = $(shell tput setaf 1)
GREEN = $(shell tput setaf 2)
YELLOW = $(shell tput setaf 3)
NC = $(shell tput sgr0)

FLAGS = -Wall -Wextra -Werror

RM = rm -f

FILES = ft_printf.c \
		ft_print_basic.c \
		ft_print_int.c \
		ft_print_usgnint.c \
		ft_print_ptr.c \
		ft_print_hexa.c \

OBJS = $(FILES:.c=.o)

.c.o : 
		@$(CC) $(FLAGS) -c $< -o $(<:.c=.o)
		@echo "$(GREEN)[$(CC)]$(NC) Compilation: $(YELLOW)$<$(NC)"

$(NAME) :	$(OBJS)
		@ar rc $(NAME) $(OBJS)
		@echo "$(GREEN)[Library]$(NC) Compilation: $(YELLOW)$(NAME)$(NC)"

all :		$(NAME)

clean :
		@$(RM) $(OBJS)
		@echo "$(RED)[Clean]$(NC) Suppression des fichiers objets"

fclean : 	clean
		@$(RM) $(NAME)
		@echo "$(RED)[Fclean]$(NC) Suppression de l'archive $(YELLOW)$(NAME)$(NC)"

re : fclean all
		@echo "$(GREEN)[Re]$(NC) Reconstruction du projet"

.PHONY: all clean fclean re
