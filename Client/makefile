CFLAGS:=-c -Wall -Weffc++ -g -std=c++11 -Iinclude -lboost_system -lboost_thread -pthread
LDFLAGS:=-lboost_system -lboost_thread -pthread

all: BGRSclient

BGRSclient: bin/connectionHandler.o bin/readAndWrite.o bin/BGRSclient.o
	@echo 'Building target: main'
	@echo 'Invoking: C++ Linker'
	g++ -o bin/BGRSclient bin/connectionHandler.o bin/readAndWrite.o bin/BGRSclient.o $(LDFLAGS)
	@echo 'Finished building target: main'
	@echo ' '

bin/BGRSclient.o: src/BGRSclient.cpp
	g++ $(CFLAGS) -o bin/BGRSclient.o src/BGRSclient.cpp

 bin/connectionHandler.o: src/connectionHandler.cpp
	g++ $(CFLAGS) -o bin/connectionHandler.o src/connectionHandler.cpp

 bin/readAndWrite.o: src/readAndWrite.cpp
	g++ $(CFLAGS) -o bin/readAndWrite.o src/readAndWrite.cpp




.PHONY: clean
clean:
	rm -f bin/*
