CC = gcc
CFLAGS = - I.

all: parallel_min_max zombie process_memory

zombie: zombie.c
	$(CC) -o zombie zombie.c
	
process_memory: process_memory.c
	$(CC) -o process_memory process_memory.c

parallel_min_max: utils.o find_min_max.o utils.h find_min_max.h
	$(CC) -o parallel_min_max utils.o find_min_max.o parallel_min_max,c $(CFLAGS)
	
utils.o : utils.h
	$(CC) -o utils.o -c utils.c

find_min_max.o: utils.h find_min_max.h
	$(CC) -o find_min_max.o -c find_min_max.c $(CFLAGS)

clean:
rm zombie process_memory parallel_min_max utils.o find_min_max.o
