CC = gcc
CFLAGS = -O2 -fPIC -Wall -bundle -undefined dynamic_lookup
#linux# -shared
#mac  # -bundle -undefined dynamic_lookup
LUADIR = ../../../skynet/3rd/lua
TARGET = protobuf.so

.PHONY : all clean

all : $(TARGET)

$(TARGET) : pbc-lua53.c
	$(CC) $(CFLAGS) -o $@ -I../.. -I$(LUADIR) -L../../build $^ -lpbc

clean :
	rm -f $(TARGET)
