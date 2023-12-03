SQUIRREL= ..


GPP= m68k-xelf-g++
OUT= $(SQUIRREL)/bin/sq.x
INCZ= -I$(SQUIRREL)/include -I. -I$(SQUIRREL)/sqlibs
LIBZ= -L$(SQUIRREL)/lib
LIB= -lsquirrel -lsqstdlib 

OBJS= sq.o

SRCS= sq.c


sq32:
	$(GPP) -O2 -fno-exceptions -fno-rtti -o $(OUT) $(SRCS) $(INCZ) -lx68k -ldos -liocs ../lib/libsquirrel.a ../lib/libsqstdlib.a
#	$(GPP) -O2 -fno-exceptions -fno-rtti -o $(OUT) $(SRCS) $(INCZ) $(LIBZ) $(LIB)

sqprof:
	$(GPP) -O2 -pg -fno-exceptions -fno-rtti -pie -gstabs -g3 -o $(OUT) $(SRCS) $(INCZ) $(LIBZ) $(LIB)

sq64:
	$(GPP) -O2 -m64 -fno-exceptions -fno-rtti -D_SQ64 -o $(OUT) $(SRCS) $(INCZ) $(LIBZ) $(LIB)
