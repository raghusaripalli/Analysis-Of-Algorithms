CC = g++ -O2 -Wall -Wno-deprecated

all: simulated_test real_test

simulated_test: MinHeap.o graph_operations.o measure_time.o graph_simulator.o simulated_test.o 
				$(CC) -o simulated_test MinHeap.o graph_operations.o measure_time.o graph_simulator.o simulated_test.o

real_test: MinHeap.o graph_operations.o graph_make.o real_test.o
				$(CC) -o real_test MinHeap.o graph_operations.o measure_time.o graph_make.o real_test.o

MinHeap.o: MinHeap.cc 
					$(CC) -g -c MinHeap.cc

graph_operations.o: graph_operations.cc 
					$(CC) -g -c graph_operations.cc

graph_simulator.o:
					$(CC) -g -c graph_simulator.cc

simulated_test.o: simulated_test.cc 
					$(CC) -g -c simulated_test.cc

measure_time.o: measure_time.cc 
					$(CC) -g -c measure_time.cc

graph_make.o: graph_make.cc 
					$(CC) -g -c graph_make.cc

real_test.o: real_test.cc
					$(CC) -g -c real_test.cc

clean: 
	rm -f *.o
	rm -f *.exe

clean_win:
	del -f *.o
	del -f *.exe