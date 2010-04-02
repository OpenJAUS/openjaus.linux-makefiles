TARGET	= 	./bin/ojNodeManager
CCFLAGS	=	-Wall -fno-strict-aliasing -O2 -c -g -I ./include/ -I ../libjaus/include/ -I ../libopenJaus/include/
LFLAGS	=	-L ../libjaus/lib/ -L ../libopenJaus/lib/
LIBS	=	-lopenJaus -ljaus -lpthread

SOURCES =	./src/main.cpp

OBJECTS =	./Build/main.o

default : all

all : $(TARGET)

clean :
	rm -f ./Build/*.o
	rm -f $(TARGET)

$(TARGET) : ./Build ./bin $(OBJECTS)
	g++ $(LFLAGS) -o $(TARGET) $(OBJECTS) $(LIBS)

./Build :
	mkdir Build

./bin :
	mkdir lib

./Build/main.o : ./src/main.cpp
	g++ $(CCFLAGS) -o ./Build/main.o ./src/main.cpp
