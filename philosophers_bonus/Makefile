NAME	= philo_bonus
CC		= gcc
CFLAGS	= -Werror -Wall -Wextra -pthread -g3

SRC_PATH = sources_bonus/
OBJ_PATH = objects_bonus/

SRC		=	main_bonus.c initialize_bonus.c checks_bonus.c \
			processus_bonus.c utils_bonus.c

SRCS	= $(addprefix $(SRC_PATH), $(SRC))
OBJ		= $(SRC:.c=.o)
OBJS	= $(addprefix $(OBJ_PATH), $(OBJ))

INC		= -I ./includes_bonus/

all: $(NAME)

$(OBJ_PATH)%.o: $(SRC_PATH)%.c
	@mkdir -p $(OBJ_PATH)
	@$(CC) $(CFLAGS) -c $< -o $@ $(INC)

$(NAME): $(OBJS)
	@$(CC) $(CFLAGS) $(OBJS) -o $@
	@echo "$$ASCII_MANDATORY";

clean:
	@rm -rf $(OBJ_PATH)

fclean: clean
	@rm -f $(NAME)
	@echo "🧽 🪣 🧹 Bonus Philosophers cleaned"

re: fclean all

.PHONY: all re clean fclean

CYN = \033[0;36m
VLT= \033[0;35m
RESET = \033[0m

info: ascii

define ASCII_MANDATORY
$(VLT)
$(VLT)██████╗ ██╗  ██╗██╗██╗      ██████╗ ███████╗ ██████╗ ██████╗ ██╗  ██╗███████╗██████╗ ███████╗$(RESET)
$(VLT)██╔══██╗██║  ██║██║██║     ██╔═══██╗██╔════╝██╔═══██╗██╔══██╗██║  ██║██╔════╝██╔══██╗██╔════╝$(RESET)
$(VLT)██████╔╝███████║██║██║     ██║   ██║███████╗██║   ██║██████╔╝███████║█████╗  ██████╔╝███████╗$(RESET)
$(VLT)██╔═══╝ ██╔══██║██║██║     ██║   ██║╚════██║██║   ██║██╔═══╝ ██╔══██║██╔══╝  ██╔══██╗╚════██║$(RESET)
$(VLT)██║     ██║  ██║██║███████╗╚██████╔╝███████║╚██████╔╝██║     ██║  ██║███████╗██║  ██║███████║$(RESET)
$(VLT)╚═╝     ╚═╝  ╚═╝╚═╝╚══════╝ ╚═════╝ ╚══════╝ ╚═════╝ ╚═╝     ╚═╝  ╚═╝╚══════╝╚═╝  ╚═╝╚══════╝$(RESET)
$(RESET)
$(VLT)			██████╗  ██████╗ ███╗   ██╗██╗   ██╗███████╗			   $(RESET)
$(VLT)			██╔══██╗██╔═══██╗████╗  ██║██║   ██║██╔════╝			   $(RESET)
$(VLT)			██████╔╝██║   ██║██╔██╗ ██║██║   ██║███████╗			   $(RESET)
$(VLT)			██╔══██╗██║   ██║██║╚██╗██║██║   ██║╚════██║			   $(RESET)
$(VLT)			██████╔╝╚██████╔╝██║ ╚████║╚██████╔╝███████║			   $(RESET)
$(VLT)			╚═════╝  ╚═════╝ ╚═╝  ╚═══╝ ╚═════╝ ╚══════╝			   $(RESET)
$(RESET)
endef
export ASCII_MANDATORY
