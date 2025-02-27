# **************************************************************************** #
#                                                                              #
#                                                         :::      ::::::::    #
#    Makefile                                           :+:      :+:    :+:    #
#                                                     +:+ +:+         +:+      #
#    By: walhamad <walhamad@student.42.fr>          +#+  +:+       +#+         #
#                                                 +#+#+#+#+#+   +#+            #
#    Created: 2024/09/04 18:09:31 by walhamad          #+#    #+#              #
#    Updated: 2024/09/04 18:09:33 by walhamad         ###   ########.fr        #
#                                                                              #
# **************************************************************************** #

#variables

NAME	= libft.a
CC	= gcc
AR	= ar rcs
HEADER	= -I libft.h
CFLAGS	= -Wall -Werror -Wextra $(HEADER)
SRCS_DIR	= srcs/
OBJS_DIR	= objs/

#Colors

DEF_COLOR = \033[0;39m
GRAY = \033[0;90m
RED = \033[0;91m
GREEN = \033[0;92m
YELLOW = \033[0;93m
BLUE = \033[0;94m
MAGENTA = \033[0;95m
CYAN = \033[0;96m
WHITE = \033[0;97m
RESET = \033[0m

#sources

SRC_FILES	= ft_isalpha ft_isdigit ft_isalnum   \
				ft_strlen ft_strlcpy   ft_strchr  ft_strncmp \
				ft_strnstr \
				ft_atoi ft_strdup ft_substr ft_strjoin ft_strtrim ft_split ft_itoa \
				ft_putchar_fd ft_putstr_fd ft_putendl_fd ft_putnbr_fd \
				ft_lstnew ft_lstadd_front ft_lstsize ft_lstlast ft_lstadd_back ft_lstdelone ft_lstclear ft_lstiter ft_lstmap \
				ft_2darrlen ft_free2darr \
				get_next_line_bonus get_next_line_utils_bonus \
				ft_strndup ft_strcmp ft_llto2darr ft_strjoin_free \
				ft_isnumber

SRCS 		= 	$(addprefix $(SRCS_DIR), $(addsuffix .c, $(SRC_FILES)))
OBJS 		= 	$(addprefix $(OBJS_DIR), $(addsuffix .o, $(SRC_FILES)))

#######

all:
		@mkdir -p $(OBJS_DIR)
		@make $(NAME)

$(OBJS_DIR)%.o:		$(SRCS_DIR)%.c
					@$(CC) $(CFLAGS) -c $< -o $@
					@echo ".\c"

$(NAME):	$(OBJS)
			@echo "\n"
			@$(AR) $(NAME) $(OBJS)
			@echo "$(GREEN)$(NAME) was created$(RESET)"

clean:
		@rm -rf $(OBJS_DIR)
		@echo "$(BLUE)$(NAME): $(YELLOW)object files are cleaned$(RESET)"

fclean:	clean
		@rm -rf $(NAME)
		@echo "$(BLUE)$(NAME): $(MAGENTA)$(NAME) was deleted$(RESET)"

re:	fclean all

.PHONY:	all clean fclean re
