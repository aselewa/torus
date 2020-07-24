CXXFLAGS?=-03
CXX?=g++
LDFLAGS?=-lm -lgsl -lgslcblas -lboost_iostreams -lz
main: main.o controller.o logistic.o 
	$(CXX)  $(CXXFLAGS) main.o controller.o logistic.o  $(LDFLAGS)  -o ../../../inst/torus 
static: main.o controller.o logistic.o
	$(CXX) $(CXXFLAGS) main.o controller.o logistic.o  $(LDFLAGS) -static -o torus.static
main.o: main.cc 
	$(CXX) -c  main.cc	
controller.o: controller.cc classdef.h
	$(CXX) -c  controller.cc 
logistic.o: logistic.cc logistic.h
	$(CXX) -c logistic.cc -fpermissive
clean:
	rm *.o torus	
