CC ?= gcc
CFLAGS ?= -Wall -Wextra -O2

INCLUDE_DIR := ../../include
LIB_DIR := ../../build/lib
COMMON_LIB := $(LIB_DIR)/libcommon.a
TARGET := backend

OBJS := main.o handler.o

all: $(TARGET)

$(TARGET): $(OBJS) $(COMMON_LIB)
	$(CC) $(CFLAGS) $(OBJS) $(COMMON_LIB) -o $(TARGET)

main.o: main.c
	$(CC) $(CFLAGS) -I$(INCLUDE_DIR) -c $< -o $@

handler.o: handler.c
	$(CC) $(CFLAGS) -I$(INCLUDE_DIR) -c $< -o $@

clean:
	rm -f $(OBJS) $(TARGET)
