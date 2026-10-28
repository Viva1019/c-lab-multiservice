CC ?= gcc
CFLAGS ?= -Wall -Wextra -O2

INCLUDE_DIR := ../include
LIB_DIR := ../build/lib
TARGET := $(LIB_DIR)/libcommon.a

OBJS := net.o http.o utils.o

all: $(TARGET)

$(LIB_DIR):
	mkdir -p $(LIB_DIR)

$(TARGET): $(OBJS) | $(LIB_DIR)
	ar rcs $@ $(OBJS)

net.o: net.c
	$(CC) $(CFLAGS) -I$(INCLUDE_DIR) -c $< -o $@

http.o: http.c
	$(CC) $(CFLAGS) -I$(INCLUDE_DIR) -c $< -o $@

utils.o: utils.c
	$(CC) $(CFLAGS) -I$(INCLUDE_DIR) -c $< -o $@

clean:
	rm -f $(OBJS) $(TARGET)
