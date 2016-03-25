CC = gcc
CFLAGS = -O2 -Wall -bundle -undefined dynamic_lookup
LUADIR = /usr/local/include
TARGET = protobuf.so

.PHONY : all clean

all : $(TARGET)

$(TARGET) : pbc-lua53.c
	$(CC) $(CFLAGS) -o $@ -I../.. -I$(LUADIR) -L../../build $^ -lpbc

clean :
	rm -f $(TARGET)