TARGET	= 	./lib/libopenJaus.so
CCFLAGS	=	-Wall -fPIC -fno-strict-aliasing -O2 -c -g -I ./include/ -I ../libjaus/include/
LFLAGS	=	-L ../libjaus/lib/
LIBS		=	-ljaus
SOURCES =  ./src/componentLibrary/ojCmpt.c ./src/nodeManagerInterface/defaultJausMessageProcessor.c ./src/nodeManagerInterface/scManager.c ./src/nodeManagerInterface/lmHandler.c ./src/nodeManagerInterface/nodeManagerInterface.c ./src/utils/streamServer.c ./src/utils/multicastSocket.c ./src/utils/streamSocket.c ./src/utils/timeLib.c ./src/utils/datagramPacket.c ./src/utils/streamPacket.c ./src/utils/queue.c ./src/utils/inetAddress.c ./src/utils/datagramSocket.c ./src/nodeManager/OjUdpComponentInterface.cpp ./src/nodeManager/JausSubsystemCommunicationManager.cpp ./src/nodeManager/MessageRouter.cpp ./src/nodeManager/JausOpcUdpInterface.cpp ./src/nodeManager/NodeManagerComponent.cpp ./src/nodeManager/LocalComponent.cpp ./src/nodeManager/events/DebugEvent.cpp ./src/nodeManager/events/NodeManagerEvent.cpp ./src/nodeManager/events/ConfigurationEvent.cpp ./src/nodeManager/events/ErrorEvent.cpp ./src/nodeManager/events/JausMessageEvent.cpp ./src/nodeManager/events/SystemTreeEvent.cpp ./src/nodeManager/JausComponentCommunicationManager.cpp ./src/nodeManager/CommunicatorComponent.cpp ./src/nodeManager/JudpInterface.cpp ./src/nodeManager/JausCommunicationManager.cpp ./src/nodeManager/JausTransportQueue.cpp ./src/nodeManager/NodeManager.cpp ./src/nodeManager/JausNodeCommunicationManager.cpp ./src/nodeManager/JausTransportInterface.cpp ./src/nodeManager/SystemTree.cpp ./src/componentLibrary/OpenJausComponent.cpp ./src/utils/FileLoader.cpp
OBJECTS =  ./Build/ojCmpt.o ./Build/defaultJausMessageProcessor.o ./Build/scManager.o ./Build/lmHandler.o ./Build/nodeManagerInterface.o ./Build/streamServer.o ./Build/multicastSocket.o ./Build/streamSocket.o ./Build/timeLib.o ./Build/datagramPacket.o ./Build/streamPacket.o ./Build/queue.o ./Build/inetAddress.o ./Build/datagramSocket.o ./Build/OjUdpComponentInterface.o ./Build/JausSubsystemCommunicationManager.o ./Build/MessageRouter.o ./Build/JausOpcUdpInterface.o ./Build/NodeManagerComponent.o ./Build/LocalComponent.o ./Build/DebugEvent.o ./Build/NodeManagerEvent.o ./Build/ConfigurationEvent.o ./Build/ErrorEvent.o ./Build/JausMessageEvent.o ./Build/SystemTreeEvent.o ./Build/JausComponentCommunicationManager.o ./Build/CommunicatorComponent.o ./Build/JudpInterface.o ./Build/JausCommunicationManager.o ./Build/JausTransportQueue.o ./Build/NodeManager.o ./Build/JausNodeCommunicationManager.o ./Build/JausTransportInterface.o ./Build/SystemTree.o ./Build/OpenJausComponent.o ./Build/FileLoader.o

default : all

all : $(TARGET)

clean :
	rm -f ./Build/*.o
	rm -f $(TARGET)

$(TARGET) : $(OBJECTS)
	g++ -shared $(LFLAGS) -o $(TARGET) $(OBJECTS) $(LIBS)

./Build/ojCmpt.o: src/componentLibrary/ojCmpt.c include/nodeManagerInterface/nodeManagerInterface.h include/utils/datagramSocket.h include/utils/inetAddress.h include/utils/datagramPacket.h include/utils/queue.h include/utils/timeLib.h include/componentLibrary/ojCmpt.h
	gcc $(CCFLAGS) -o ./Build/ojCmpt.o ./src/componentLibrary/ojCmpt.c

./Build/defaultJausMessageProcessor.o: src/nodeManagerInterface/defaultJausMessageProcessor.c include/nodeManagerInterface/nodeManagerInterface.h include/utils/datagramSocket.h include/utils/inetAddress.h include/utils/datagramPacket.h include/utils/queue.h include/utils/timeLib.h
	gcc $(CCFLAGS) -o ./Build/defaultJausMessageProcessor.o ./src/nodeManagerInterface/defaultJausMessageProcessor.c

./Build/scManager.o: src/nodeManagerInterface/scManager.c include/nodeManagerInterface/nodeManagerInterface.h include/utils/datagramSocket.h include/utils/inetAddress.h include/utils/datagramPacket.h include/utils/queue.h include/utils/timeLib.h
	gcc $(CCFLAGS) -o ./Build/scManager.o ./src/nodeManagerInterface/scManager.c

./Build/lmHandler.o: src/nodeManagerInterface/lmHandler.c include/nodeManagerInterface/nodeManagerInterface.h include/utils/datagramSocket.h include/utils/inetAddress.h include/utils/datagramPacket.h include/utils/queue.h include/utils/timeLib.h
	gcc $(CCFLAGS) -o ./Build/lmHandler.o ./src/nodeManagerInterface/lmHandler.c

./Build/nodeManagerInterface.o: src/nodeManagerInterface/nodeManagerInterface.c include/nodeManagerInterface/nodeManagerInterface.h include/utils/datagramSocket.h include/utils/inetAddress.h include/utils/datagramPacket.h include/utils/queue.h include/utils/timeLib.h
	gcc $(CCFLAGS) -o ./Build/nodeManagerInterface.o ./src/nodeManagerInterface/nodeManagerInterface.c

./Build/streamServer.o: src/utils/streamServer.c include/utils/streamServer.h include/utils/inetAddress.h include/utils/streamPacket.h
	gcc $(CCFLAGS) -o ./Build/streamServer.o ./src/utils/streamServer.c

./Build/multicastSocket.o: src/utils/multicastSocket.c include/utils/multicastSocket.h include/utils/inetAddress.h include/utils/datagramSocket.h include/utils/datagramPacket.h
	gcc $(CCFLAGS) -o ./Build/multicastSocket.o ./src/utils/multicastSocket.c

./Build/streamSocket.o: src/utils/streamSocket.c include/utils/streamSocket.h include/utils/inetAddress.h include/utils/streamPacket.h
	gcc $(CCFLAGS) -o ./Build/streamSocket.o ./src/utils/streamSocket.c

./Build/timeLib.o: src/utils/timeLib.c include/utils/timeLib.h
	gcc $(CCFLAGS) -o ./Build/timeLib.o ./src/utils/timeLib.c

./Build/datagramPacket.o: src/utils/datagramPacket.c include/utils/datagramPacket.h include/utils/inetAddress.h
	gcc $(CCFLAGS) -o ./Build/datagramPacket.o ./src/utils/datagramPacket.c

./Build/streamPacket.o: src/utils/streamPacket.c include/utils/streamPacket.h include/utils/inetAddress.h
	gcc $(CCFLAGS) -o ./Build/streamPacket.o ./src/utils/streamPacket.c

./Build/queue.o: src/utils/queue.c include/utils/queue.h
	gcc $(CCFLAGS) -o ./Build/queue.o ./src/utils/queue.c

./Build/inetAddress.o: src/utils/inetAddress.c include/utils/inetAddress.h
	gcc $(CCFLAGS) -o ./Build/inetAddress.o ./src/utils/inetAddress.c

./Build/datagramSocket.o: src/utils/datagramSocket.c include/utils/datagramSocket.h include/utils/inetAddress.h include/utils/datagramPacket.h
	gcc $(CCFLAGS) -o ./Build/datagramSocket.o ./src/utils/datagramSocket.c

./Build/OjUdpComponentInterface.o: src/nodeManager/OjUdpComponentInterface.cpp include/nodeManager/OjUdpComponentInterface.h include/nodeManager/JausTransportInterface.h include/nodeManager/JausTransportQueue.h include/nodeManager/EventHandler.h include/nodeManager/events/NodeManagerEvent.h include/nodeManager/SystemTree.h include/utils/FileLoader.h include/nodeManager/JausComponentCommunicationManager.h include/nodeManager/JausCommunicationManager.h include/utils/hashMap.h include/nodeManager/MessageRouter.h include/nodeManager/NodeManagerComponent.h include/nodeManager/LocalComponent.h include/nodeManager/CommunicatorComponent.h include/utils/datagramSocket.h include/utils/inetAddress.h include/utils/datagramPacket.h include/nodeManager/events/ErrorEvent.h include/nodeManager/events/NodeManagerEvent.h
	g++ $(CCFLAGS) -o ./Build/OjUdpComponentInterface.o ./src/nodeManager/OjUdpComponentInterface.cpp

./Build/JausSubsystemCommunicationManager.o: src/nodeManager/JausSubsystemCommunicationManager.cpp include/nodeManager/JausSubsystemCommunicationManager.h include/nodeManager/JausCommunicationManager.h include/nodeManager/JausTransportInterface.h include/nodeManager/JausTransportQueue.h include/nodeManager/EventHandler.h include/nodeManager/events/NodeManagerEvent.h include/nodeManager/SystemTree.h include/utils/FileLoader.h include/utils/hashMap.h include/nodeManager/MessageRouter.h include/nodeManager/JausOpcUdpInterface.h include/utils/multicastSocket.h include/utils/inetAddress.h include/utils/datagramSocket.h include/utils/datagramPacket.h include/nodeManager/JudpInterface.h include/nodeManager/events/ErrorEvent.h include/nodeManager/events/NodeManagerEvent.h include/nodeManager/events/ConfigurationEvent.h
	g++ $(CCFLAGS) -o ./Build/JausSubsystemCommunicationManager.o ./src/nodeManager/JausSubsystemCommunicationManager.cpp

./Build/MessageRouter.o: src/nodeManager/MessageRouter.cpp include/nodeManager/MessageRouter.h include/nodeManager/EventHandler.h include/nodeManager/events/NodeManagerEvent.h include/nodeManager/SystemTree.h include/utils/FileLoader.h include/nodeManager/JausSubsystemCommunicationManager.h include/nodeManager/JausCommunicationManager.h include/nodeManager/JausTransportInterface.h include/nodeManager/JausTransportQueue.h include/utils/hashMap.h include/nodeManager/MessageRouter.h include/nodeManager/JausNodeCommunicationManager.h include/nodeManager/JausComponentCommunicationManager.h include/nodeManager/NodeManagerComponent.h include/nodeManager/LocalComponent.h include/nodeManager/CommunicatorComponent.h include/nodeManager/events/ErrorEvent.h include/nodeManager/events/NodeManagerEvent.h
	g++ $(CCFLAGS) -o ./Build/MessageRouter.o ./src/nodeManager/MessageRouter.cpp

./Build/JausOpcUdpInterface.o: src/nodeManager/JausOpcUdpInterface.cpp include/nodeManager/JausOpcUdpInterface.h include/nodeManager/JausTransportInterface.h include/nodeManager/JausTransportQueue.h include/nodeManager/EventHandler.h include/nodeManager/events/NodeManagerEvent.h include/nodeManager/SystemTree.h include/utils/FileLoader.h include/utils/hashMap.h include/utils/multicastSocket.h include/utils/inetAddress.h include/utils/datagramSocket.h include/utils/datagramPacket.h include/nodeManager/JausSubsystemCommunicationManager.h include/nodeManager/JausCommunicationManager.h include/nodeManager/MessageRouter.h include/nodeManager/JausNodeCommunicationManager.h include/nodeManager/JausComponentCommunicationManager.h include/nodeManager/NodeManagerComponent.h include/nodeManager/LocalComponent.h include/nodeManager/CommunicatorComponent.h include/nodeManager/events/ErrorEvent.h include/nodeManager/events/NodeManagerEvent.h include/nodeManager/events/JausMessageEvent.h include/nodeManager/JausTransportInterface.h
	g++ $(CCFLAGS) -o ./Build/JausOpcUdpInterface.o ./src/nodeManager/JausOpcUdpInterface.cpp

./Build/NodeManagerComponent.o: src/nodeManager/NodeManagerComponent.cpp include/nodeManager/NodeManagerComponent.h include/nodeManager/LocalComponent.h include/nodeManager/JausTransportInterface.h include/nodeManager/JausTransportQueue.h include/nodeManager/EventHandler.h include/nodeManager/events/NodeManagerEvent.h include/nodeManager/SystemTree.h include/utils/FileLoader.h include/utils/hashMap.h include/nodeManager/JausComponentCommunicationManager.h include/nodeManager/JausCommunicationManager.h include/nodeManager/MessageRouter.h include/nodeManager/NodeManagerComponent.h include/nodeManager/CommunicatorComponent.h include/nodeManager/events/SystemTreeEvent.h include/nodeManager/events/NodeManagerEvent.h include/nodeManager/events/ErrorEvent.h include/nodeManager/events/DebugEvent.h include/nodeManager/EventHandler.h include/nodeManager/SystemTree.h include/utils/timeLib.h
	g++ $(CCFLAGS) -o ./Build/NodeManagerComponent.o ./src/nodeManager/NodeManagerComponent.cpp

./Build/LocalComponent.o: src/nodeManager/LocalComponent.cpp include/nodeManager/LocalComponent.h include/nodeManager/JausTransportInterface.h include/nodeManager/JausTransportQueue.h include/nodeManager/EventHandler.h include/nodeManager/events/NodeManagerEvent.h include/nodeManager/SystemTree.h include/utils/FileLoader.h include/utils/timeval.h
	g++ $(CCFLAGS) -o ./Build/LocalComponent.o ./src/nodeManager/LocalComponent.cpp

./Build/DebugEvent.o: src/nodeManager/events/DebugEvent.cpp include/nodeManager/events/DebugEvent.h include/nodeManager/events/NodeManagerEvent.h
	g++ $(CCFLAGS) -o ./Build/DebugEvent.o ./src/nodeManager/events/DebugEvent.cpp

./Build/NodeManagerEvent.o: src/nodeManager/events/NodeManagerEvent.cpp include/nodeManager/events/NodeManagerEvent.h
	g++ $(CCFLAGS) -o ./Build/NodeManagerEvent.o ./src/nodeManager/events/NodeManagerEvent.cpp

./Build/ConfigurationEvent.o: src/nodeManager/events/ConfigurationEvent.cpp include/nodeManager/events/ConfigurationEvent.h include/nodeManager/events/NodeManagerEvent.h
	g++ $(CCFLAGS) -o ./Build/ConfigurationEvent.o ./src/nodeManager/events/ConfigurationEvent.cpp

./Build/ErrorEvent.o: src/nodeManager/events/ErrorEvent.cpp include/nodeManager/events/ErrorEvent.h include/nodeManager/events/NodeManagerEvent.h
	g++ $(CCFLAGS) -o ./Build/ErrorEvent.o ./src/nodeManager/events/ErrorEvent.cpp

./Build/JausMessageEvent.o: src/nodeManager/events/JausMessageEvent.cpp include/nodeManager/events/JausMessageEvent.h include/nodeManager/events/NodeManagerEvent.h include/nodeManager/JausTransportInterface.h include/nodeManager/JausTransportQueue.h include/nodeManager/EventHandler.h include/nodeManager/SystemTree.h include/utils/FileLoader.h
	g++ $(CCFLAGS) -o ./Build/JausMessageEvent.o ./src/nodeManager/events/JausMessageEvent.cpp

./Build/SystemTreeEvent.o: src/nodeManager/events/SystemTreeEvent.cpp include/nodeManager/events/SystemTreeEvent.h include/nodeManager/events/NodeManagerEvent.h
	g++ $(CCFLAGS) -o ./Build/SystemTreeEvent.o ./src/nodeManager/events/SystemTreeEvent.cpp

./Build/JausComponentCommunicationManager.o: src/nodeManager/JausComponentCommunicationManager.cpp include/nodeManager/JausComponentCommunicationManager.h include/nodeManager/JausCommunicationManager.h include/nodeManager/JausTransportInterface.h include/nodeManager/JausTransportQueue.h include/nodeManager/EventHandler.h include/nodeManager/events/NodeManagerEvent.h include/nodeManager/SystemTree.h include/utils/FileLoader.h include/utils/hashMap.h include/nodeManager/MessageRouter.h include/nodeManager/NodeManagerComponent.h include/nodeManager/LocalComponent.h include/nodeManager/CommunicatorComponent.h include/nodeManager/NodeManagerComponent.h include/nodeManager/CommunicatorComponent.h include/nodeManager/JausOpcUdpInterface.h include/utils/multicastSocket.h include/utils/inetAddress.h include/utils/datagramSocket.h include/utils/datagramPacket.h include/nodeManager/JudpInterface.h include/nodeManager/OjUdpComponentInterface.h include/nodeManager/JausComponentCommunicationManager.h include/nodeManager/events/ErrorEvent.h include/nodeManager/events/NodeManagerEvent.h include/nodeManager/events/ConfigurationEvent.h
	g++ $(CCFLAGS) -o ./Build/JausComponentCommunicationManager.o ./src/nodeManager/JausComponentCommunicationManager.cpp

./Build/CommunicatorComponent.o: src/nodeManager/CommunicatorComponent.cpp include/nodeManager/CommunicatorComponent.h include/utils/hashMap.h include/nodeManager/LocalComponent.h include/nodeManager/JausTransportInterface.h include/nodeManager/JausTransportQueue.h include/nodeManager/EventHandler.h include/nodeManager/events/NodeManagerEvent.h include/nodeManager/SystemTree.h include/utils/FileLoader.h include/nodeManager/JausComponentCommunicationManager.h include/nodeManager/JausCommunicationManager.h include/nodeManager/MessageRouter.h include/nodeManager/NodeManagerComponent.h include/nodeManager/CommunicatorComponent.h include/nodeManager/events/ErrorEvent.h include/nodeManager/events/NodeManagerEvent.h include/nodeManager/events/DebugEvent.h include/nodeManager/EventHandler.h include/utils/timeLib.h
	g++ $(CCFLAGS) -o ./Build/CommunicatorComponent.o ./src/nodeManager/CommunicatorComponent.cpp

./Build/JudpInterface.o: src/nodeManager/JudpInterface.cpp include/nodeManager/JudpInterface.h include/nodeManager/JausTransportInterface.h include/nodeManager/JausTransportQueue.h include/nodeManager/EventHandler.h include/nodeManager/events/NodeManagerEvent.h include/nodeManager/SystemTree.h include/utils/FileLoader.h include/utils/multicastSocket.h include/utils/inetAddress.h include/utils/datagramSocket.h include/utils/datagramPacket.h include/utils/hashMap.h include/nodeManager/JausSubsystemCommunicationManager.h include/nodeManager/JausCommunicationManager.h include/nodeManager/MessageRouter.h include/nodeManager/JausNodeCommunicationManager.h include/nodeManager/JausComponentCommunicationManager.h include/nodeManager/NodeManagerComponent.h include/nodeManager/LocalComponent.h include/nodeManager/CommunicatorComponent.h include/nodeManager/events/ErrorEvent.h include/nodeManager/events/NodeManagerEvent.h include/nodeManager/events/JausMessageEvent.h include/nodeManager/JausTransportInterface.h
	g++ $(CCFLAGS) -o ./Build/JudpInterface.o ./src/nodeManager/JudpInterface.cpp

./Build/JausCommunicationManager.o: src/nodeManager/JausCommunicationManager.cpp include/nodeManager/JausCommunicationManager.h include/nodeManager/JausTransportInterface.h include/nodeManager/JausTransportQueue.h include/nodeManager/EventHandler.h include/nodeManager/events/NodeManagerEvent.h include/nodeManager/SystemTree.h include/utils/FileLoader.h include/utils/hashMap.h include/nodeManager/MessageRouter.h include/nodeManager/JausTransportInterface.h
	g++ $(CCFLAGS) -o ./Build/JausCommunicationManager.o ./src/nodeManager/JausCommunicationManager.cpp

./Build/JausTransportQueue.o: src/nodeManager/JausTransportQueue.cpp include/nodeManager/JausTransportQueue.h include/nodeManager/JausTransportInterface.h include/nodeManager/JausTransportQueue.h include/nodeManager/EventHandler.h include/nodeManager/events/NodeManagerEvent.h include/nodeManager/SystemTree.h include/utils/FileLoader.h include/nodeManager/JausCommunicationManager.h include/nodeManager/JausTransportInterface.h include/utils/hashMap.h include/nodeManager/MessageRouter.h
	g++ $(CCFLAGS) -o ./Build/JausTransportQueue.o ./src/nodeManager/JausTransportQueue.cpp

./Build/NodeManager.o: src/nodeManager/NodeManager.cpp include/nodeManager/NodeManager.h include/nodeManager/MessageRouter.h include/nodeManager/EventHandler.h include/nodeManager/events/NodeManagerEvent.h include/nodeManager/SystemTree.h include/utils/FileLoader.h include/nodeManager/events/NodeManagerEvent.h include/nodeManager/events/SystemTreeEvent.h include/nodeManager/events/NodeManagerEvent.h include/nodeManager/events/ErrorEvent.h include/nodeManager/events/JausMessageEvent.h include/nodeManager/JausTransportInterface.h include/nodeManager/JausTransportQueue.h include/nodeManager/events/DebugEvent.h include/nodeManager/events/ConfigurationEvent.h
	g++ $(CCFLAGS) -o ./Build/NodeManager.o ./src/nodeManager/NodeManager.cpp

./Build/JausNodeCommunicationManager.o: src/nodeManager/JausNodeCommunicationManager.cpp include/nodeManager/JausNodeCommunicationManager.h include/nodeManager/JausCommunicationManager.h include/nodeManager/JausTransportInterface.h include/nodeManager/JausTransportQueue.h include/nodeManager/EventHandler.h include/nodeManager/events/NodeManagerEvent.h include/nodeManager/SystemTree.h include/utils/FileLoader.h include/utils/hashMap.h include/nodeManager/MessageRouter.h include/nodeManager/JausOpcUdpInterface.h include/utils/multicastSocket.h include/utils/inetAddress.h include/utils/datagramSocket.h include/utils/datagramPacket.h include/nodeManager/JudpInterface.h include/nodeManager/events/ErrorEvent.h include/nodeManager/events/NodeManagerEvent.h include/nodeManager/events/ConfigurationEvent.h
	g++ $(CCFLAGS) -o ./Build/JausNodeCommunicationManager.o ./src/nodeManager/JausNodeCommunicationManager.cpp

./Build/JausTransportInterface.o: src/nodeManager/JausTransportInterface.cpp include/nodeManager/JausTransportInterface.h include/nodeManager/JausTransportQueue.h include/nodeManager/EventHandler.h include/nodeManager/events/NodeManagerEvent.h include/nodeManager/SystemTree.h include/utils/FileLoader.h include/nodeManager/JausCommunicationManager.h include/nodeManager/JausTransportInterface.h include/utils/hashMap.h include/nodeManager/MessageRouter.h
	g++ $(CCFLAGS) -o ./Build/JausTransportInterface.o ./src/nodeManager/JausTransportInterface.cpp

./Build/SystemTree.o: src/nodeManager/SystemTree.cpp include/nodeManager/SystemTree.h include/utils/FileLoader.h include/nodeManager/EventHandler.h include/nodeManager/events/NodeManagerEvent.h include/utils/timeLib.h include/nodeManager/events/SystemTreeEvent.h include/nodeManager/events/NodeManagerEvent.h
	g++ $(CCFLAGS) -o ./Build/SystemTree.o ./src/nodeManager/SystemTree.cpp

./Build/OpenJausComponent.o: src/componentLibrary/OpenJausComponent.cpp include/componentLibrary/OpenJausComponent.h
	g++ $(CCFLAGS) -o ./Build/OpenJausComponent.o ./src/componentLibrary/OpenJausComponent.cpp

./Build/FileLoader.o: src/utils/FileLoader.cpp include/utils/FileLoader.h
	g++ $(CCFLAGS) -o ./Build/FileLoader.o ./src/utils/FileLoader.cpp
