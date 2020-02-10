CC=g++

CFLAGS= -C -Wall

all: escape_room

escape_room: main.cpp main.h menu.cpp puzzle_logic.cpp room1.cpp room2.cpp
	$(CC) main.o menu.o puzzle_logic.o room1.o room2.o -o escape_room

main.o: main.cpp
	$(CC) $(CFLAGS) main.cpp

menu.o: menu.cpp
	$(CC) $(CFLAGS) menu.cpp

puzzle_logic.o: puzzle_logic.cpp
	$(CC) $(CFLAGS) puzzle_Logic.cpp

room1.o: room1.cpp
	$(CC) $(CFLAGS) room1.cpp

room2.o: room2.cpp
	$(CC) $(CFLAGS) room2.cpp

clean:
	rm -rf *o escape_room