# Makefile for playmus and playwave

CC = gcc
CFLAGS = $(shell pkgconf --cflags sdl3 sdl3-mixer) -Wall -O
LIBS = $(shell pkgconf --libs sdl3 sdl3-mixer)
EXE = playmus playwave

all: $(EXE)

playmus: playmus.c Makefile
	$(CC) -o $@ $@.c $(CFLAGS) $(LIBS)

playwave: playwave.c Makefile
	$(CC) -o $@ $@.c $(CFLAGS) $(LIBS)

clean:
	-rm *.o $(EXE)
