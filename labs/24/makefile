# Makefile for Lab 24
CXX = g++
MAIN = lab_24
CPP_FILES = bst_node.cpp bs_tree.cpp
H_FILES = bst_node.h bs_tree.h
CXXFLAGS = -Wall -Wextra -pedantic -g

# Type 'make' to create the executable
${MAIN}: ${MAIN}.cpp ${H_FILES} ${CPP_FILES}
	${CXX} ${CXXFLAGS} ${MAIN}.cpp ${CPP_FILES} -o $@
	@echo 'Use ./${MAIN} to run'

# Type 'make style' to check your code style
style: ../../helpful_files/cpplint.py ${FILE} 
	python2 $< --filter=-runtime/references,-legal/copyright,-readability/streams,-runtime/explicit,-build/header_guard,-build/include ${MAIN}.cpp ${H_FILES} ${CPP_FILES}

# Type 'make clean' to remove the executable
clean:
	rm -rf ${MAIN}
