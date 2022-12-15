#CXX = g++
#CXX = clang++

CLIENT_EXE = chat_client
SERVER_EXE = chat_server

BOOST_DIR = /opt/homebrew/Cellar/boost/1.80.0

CLIENT_SOURCE = chat_client.cpp 
SERVER_SOURCE = chat_server.cpp

CLIENT_OBJS = $(addsuffix .o, $(basename $(notdir $(CLIENT_SOURCE))))
SERVER_OBJS = $(addsuffix .o, $(basename $(notdir $(SERVER_SOURCE))))

UNAME_S := $(shell uname -s)
LINUX_GL_LIBS = -lGL

CXXFLAGS = -std=c++17 -I$(BOOST_DIR)/include
CXXFLAGS += -g -Wall -Wformat
LIBS =

##---------------------------------------------------------------------
## BUILD RULES
##---------------------------------------------------------------------

all: $(CLIENT_EXE) $(SERVER_EXE)
	@echo Build complete :P

$(CLIENT_EXE): $(CLIENT_OBJS)
	$(CXX) -o $@ $^ $(CXXFLAGS) $(LIBS)

$(SERVER_EXE): $(SERVER_OBJS)
	$(CXX) -o $@ $^ $(CXXFLAGS) $(LIBS)

clean:
	rm -f $(CLIENT_EXE) $(CLIENT_OBJS) $(SERVER_EXE) $(SERVER_OBJS)