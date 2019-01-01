all: camera recv_csi
OBJS = csi_fun.o main.o
CC = gcc
LDLIBS = -I. `pkg-config --cflags --libs opencv`
recv_csi: $(OBJS)
	$(CC) $(OBJS) -o recv_csi
csi_fun.o: csi_fun.c csi_fun.h
	$(CC) -c csi_fun.c -o csi_fun.o
main.o: main.c csi_fun.h
	$(CC) -c main.c -o main.o
camera.cpp: 
clean: 
	rm -f *.o recv_csi

