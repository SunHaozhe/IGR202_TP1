CIBLE = main
SRCS =  Main.cpp Camera.cpp Mesh.cpp GLProgram.cpp GLShader.cpp GLError.cpp LightSource.cpp Ray.cpp BVH.cpp OctreeNode.cpp
OPENGL_PATH = /usr/lib/nvidia-367 # change this for your own environment
LIBS = -L$(OPENGL_PATH) -lglut -lGLU -lGL -lm -lpthread /usr/lib/x86_64-linux-gnu/libGLEW.so.2.0

CC = g++
CPP = g++

FLAGS = -Wall -g -pthread

CFLAGS = $(FLAGS)
CXXFLAGS = $(FLAGS)

OBJS = $(SRCS:.cpp=.o)

$(CIBLE): $(OBJS)
	g++ $(LDFLAGS) -o $(CIBLE) $(OBJS) $(LIBS)
clean:
	rm -f  *~  $(CIBLE) $(OBJS)

Camera.o: Camera.cpp Camera.h Vec3.h
Mesh.o: Mesh.cpp Mesh.h Vec3.h
GLError.o: GLError.cpp GLError.h Exception.h
GLShader.o: GLShader.cpp GLShader.h GLError.h
GLProgram.o: GLProgram.cpp GLProgram.h GLShader.h GLError.h Exception.h
Main.o: Main.cpp Vec3.h Camera.h Mesh.h GLProgram.h Exception.h
