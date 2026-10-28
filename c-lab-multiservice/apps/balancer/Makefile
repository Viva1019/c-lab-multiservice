CC ?= gcc
CFLAGS ?= -Wall -Wextra -O2

INCLUDE_DIR := ../../include
LIB_DIR := ../../build/lib
COMMON_LIB := $(LIB_DIR)/libcommon.a
TARGET := balancer

OBJS := main.o router.o

all: $(TARGET)

$(TARGET): $(OBJS) $(COMMON_LIB)
	$(CC) $(CFLAGS) $(OBJS) $(COMMON_LIB) -o $(TARGET)

main.o: main.c
	$(CC) $(CFLAGS) -I$(INCLUDE_DIR) -c $< -o $@

router.o: router.c
	$(CC) $(CFLAGS) -I$(INCLUDE_DIR) -c $< -o $@

clean:
	rm -f $(OBJS) $(TARGET)
