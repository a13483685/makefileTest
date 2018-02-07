.PHONY:all clean

SRCS = $(wildcard *.c)
OBJS = $(SRCS:.c=.o)
DEPS = $(SRCS:.c=.d)
BIN = 
all: $(DEPS) $(OBJS) $(BIN)
$(BIN):$(OBJS)
	@echo "start1 $(SRCS)"
	gcc -o $@ $^
%.o:%.c
	@echo "start2 $(SRCS)"
	gcc -o $@ -c $(filter %.c,$^)
%.d:%.c
	@echo "start3 $(SRCS)"
	gcc -MM $^ > $@
clean:
	rm -f $(BIN) $(OBJS) $(DEPS)

