# 4. Write a Makefile which includes:
#
# * A default target which builds the “writer” application
# * A clean target which removes the “writer” application and all .o files
# * Support for cross-compilation.  You should be able to generate an application for the native build platform when 
#    GNU make variable CROSS_COMPILE is not specified on the make command line.  When CROSS_COMPILE is specified with 
#    aarch64-none-linux-gnu- (note the trailing -)your makefile should compile successfully using the cross compiler 
#    installed in step 1.

# References
# * 21st Century C, 2nd edition, by Ben Klemens. O'Reilly, September 2014.
# * The GNU Make Manual, for GNU make version 4.4.1, by the Free Software 
#   Foundation. Self-published, February 2023.
#

# TODO: clean target and cross-compile target

P=writer
SOURCES= writer.c
OBJECTS= $(SOURCES:.c=.o)
CFLAGS= -g -Wall -O3 -std=c11  # none of that old ANSI stuff please
CC=$(CROSS_COMPILE)gcc #if the variable is undefined, this will default to "gcc"

all: $(P)
$(P): $(OBJECTS)
	$(CC) $(CFLAGS) -o $(P) $(OBJECTS)

clean:
	rm -f $(OBJECTS) $(P)
