CC=g++
CFLAGS=-std=c++20
LDFLAGS=-lmata

NAME1=bench-automata-simulation
NAME2=testing-simulation

LINK=utils/utils.cc

.PHONY: all

all: $(NAME1) $(NAME2)

$(NAME1): $(NAME1).cc
	$(CC) $(CFLAGS) $(NAME1).cc $(LINK) -o $(NAME1) $(LDFLAGS)

$(NAME2): $(NAME2).cc
	$(CC) $(CFLAGS) $(NAME2).cc $(LINK) -o $(NAME2) $(LDFLAGS)
