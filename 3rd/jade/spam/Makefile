
#############################################################################
# Makefile for building spam
# Generated by tmake at 14:28, 1999/10/06
#     Project: spam
#    Template: ../pro/japp
#############################################################################

####### Compiler, tools and options

CC	=	egcs
CXX	=	eg++
CFLAGS	=	-pipe -O2 -fno-strength-reduce
CXXFLAGS=	-DSTDC_HEADERS=1 \
-DHAVE_LIMITS_H=1 -DHAVE_ST_BLKSIZE=1 -O2 -fno-strength-reduce
INCPATH	=	-I../sp -I../generic
LINK	=	eg++ -pthread
LFLAGS	=	
LIBS	=	-L../libs -lsp
MOC	=	moc

TAR	=	tar -cf
GZIP	=	gzip -9f

####### Files

HEADERS =	CopyEventHandler.h \
		MarkupEventHandler.h \
		SpamMessages.h
SOURCES =	CopyEventHandler.cxx \
		MarkupEventHandler.cxx \
		spam.cxx \
		spam_inst.cxx
OBJECTS =	CopyEventHandler.o \
		MarkupEventHandler.o \
		spam.o \
		spam_inst.o
SRCMOC	=	
OBJMOC	=	
DIST	=	
TARGET	=	spam

####### Implicit rules

.SUFFIXES: .cpp .cxx .cc .C .c

.cpp.o:
	$(CXX) -c $(CXXFLAGS) $(INCPATH) -o $@ $<

.cxx.o:
	$(CXX) -c $(CXXFLAGS) $(INCPATH) -o $@ $<

.cc.o:
	$(CXX) -c $(CXXFLAGS) $(INCPATH) -o $@ $<

.C.o:
	$(CXX) -c $(CXXFLAGS) $(INCPATH) -o $@ $<

.c.o:
	$(CC) -c $(CFLAGS) $(INCPATH) -o $@ $<

####### Build rules

all: $(TARGET)

$(TARGET): $(OBJECTS) $(OBJMOC) 
	$(LINK) $(LFLAGS) -o $(TARGET) $(OBJECTS) $(OBJMOC) $(LIBS)

moc: $(SRCMOC)

tmake:
	tmake spam.pro

dist:
	$(TAR) spam.tar spam.pro $(SOURCES) $(HEADERS) $(DIST)
	$(GZIP) spam.tar

clean:
	-rm -f $(OBJECTS) $(OBJMOC) $(SRCMOC) $(TARGET)
	-rm -f *~ core

####### Compile

CopyEventHandler.o: CopyEventHandler.cxx \
		CopyEventHandler.h \
		MarkupEventHandler.h

MarkupEventHandler.o: MarkupEventHandler.cxx \
		MarkupEventHandler.h

spam.o: spam.cxx \
		SpamMessages.h \
		CopyEventHandler.h \
		MarkupEventHandler.h

spam_inst.o: spam_inst.cxx \
		CopyEventHandler.h \
		MarkupEventHandler.h



