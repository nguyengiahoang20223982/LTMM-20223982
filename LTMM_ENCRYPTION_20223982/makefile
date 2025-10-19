CC = gcc
DEPS = rc4_encrypt.h rc4_init.h rc4_stream.h
CFLAGS = -Wall -std=c99 -D__USE_MINGW_ANSI_STDIO=1

%.o: %.c $(DEPS)
	$(CC) -c $< $(CFLAGS) -o $@

all: main.o rc4_encrypt.o rc4_init.o rc4_stream.o
	$(CC) -o main main.o rc4_encrypt.o rc4_init.o rc4_stream.o $(CFLAGS)

clean:
	del /Q *.o main.exe
