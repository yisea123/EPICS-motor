# Makefile
TOP = ../..
include $(TOP)/configure/CONFIG

# Both the following line, and a line in the *.dbd file,
# must be uncommented to use diagnostic debugging messages.
USR_CXXFLAGS += -DDEBUG

DBD += devMclennanMotor.dbd
DBD += homing.dbd

LIBRARY_IOC = Mclennan

# Intelligent Motion Systems driver support.
SRCS += MclennanRegister.cc
SRCS += homing.st
SRCS += devPM304.cc drvPM304.cc

Mclennan_LIBS += motor
Mclennan_LIBS += asyn
Mclennan_LIBS += seq
Mclennan_LIBS += pv
Mclennan_LIBS += $(EPICS_BASE_IOC_LIBS)

include $(TOP)/configure/RULES

