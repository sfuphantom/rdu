# compiler
CC=gcc
# executable name
OUT=lcdapp
# non-standard include paths
INC= -I../
# compiler flags
CFLAGS= -g -std=c99 -Wall -c
# libraries
LIBS= -lrt -pthread
# object file directory
OBJDIR=obj
# object files
OBJS= $(addprefix $(OBJDIR)/, \
	lcdtask.o)


all: directories $(OUT)


$(OUT): $(OBJS)
	$(CC) -g -o $(OUT) $^ $(LIBS)

$(OBJDIR)/%.o: %.c
	$(CC) $(CFLAGS) $(INC) -o $@ $<


.PHONY: directories
directories:
	mkdir -p $(OBJDIR)

.PHONY: clean
clean:
	rm $(OBJDIR)/*.o $(OUT)

