#
# Makefile
#

CIRCLEHOME = ../Circle

INCLUDE	+= -I ./include
INCLUDE	+= -I ../lib-artnet/include -I ../lib-lightset/include

OBJS	= src/dmxsend.o

EXTRACLEAN = src/*.o

libdmx.a: $(OBJS)
	rm -f $@
	$(AR) cr $@ $(OBJS)
	$(PREFIX)objdump -D libdmx.a | $(PREFIX)c++filt > libdmx.lst

include $(CIRCLEHOME)/Rules.mk
