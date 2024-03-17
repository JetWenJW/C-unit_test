#Name of component under test
COMPONENT_NAME = average

#Dynamically generate absolute path
#FROM ...
MAKEFILE_DIR = $(dir $(realpath $(firstword $(MAKEFILE_LIST))))
PROJECT_DIR =$(realpath $(MAKEFILE_DIR)../..)
SRC_DIR = $(PROJECT_DIR)/src
TEST_DIR = $(PROJECT_DIR)/tests

#Location of CppUTest(if not already set)
CPPUTEST_HOME ?= $(PROJECT_DIR)/tools/cpputest

#include and source files for component under tests
INCLUDE_DIRS = $(SRC_DIR)/$(COMPONENT_NAME)
SRC_DIRS = $(SRC_DIR)/$(COMPONENT_NAME)

#include CppUTest header files
INCLUDE_DIRS += $(CPPUTEST_HOME)/include

#Directories containing the unit tests
TEST_SRC_DIRS = $(TEST_DIR)/$(COMPONENT_NAME)

#Include makefile worker
include $(CPPUTEST_HOME)/build/MakefileWorker.mk