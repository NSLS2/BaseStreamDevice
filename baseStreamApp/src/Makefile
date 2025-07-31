TOP=../..

include $(TOP)/configure/CONFIG
#----------------------------------------
#  ADD MACRO DEFINITIONS AFTER THIS LINE
#=============================
# Build the IOC application

PROD_NAME = baseStream

PROD_IOC = $(PROD_NAME)App

# $(PROD_IOC).dbd will be created and installed
DBD += $(PROD_IOC).dbd

# $(PROD_IOC).dbd will be made up from these files:
$(PROD_IOC)_DBD += base.dbd
$(PROD_IOC)_DBD += asyn.dbd
$(PROD_IOC)_DBD += busySupport.dbd
$(PROD_IOC)_DBD += drvAsynIPPort.dbd drvAsynSerialPort.dbd drvVxi11.dbd
$(PROD_IOC)_DBD += calc.dbd calcSupport.dbd
$(PROD_IOC)_DBD += stream.dbd
$(PROD_IOC)_DBD += asSupport.dbd
$(PROD_IOC)_DBD += devIocStats.dbd
$(PROD_IOC)_DBD += calcSupport.dbd


# Add all the support libraries needed by this IOC
$(PROD_IOC)_LIBS += asyn busy calc stream autosave devIocStats reccaster

$(PROD_IOC)_SRCS += $(PROD_IOC)_registerRecordDeviceDriver.cpp

$(PROD_IOC)_SRCS += $(PROD_IOC)Main.cpp

$(PROD_IOC)_LIBS += $(EPICS_BASE_IOC_LIBS)

#=============================

include $(TOP)/configure/RULES
#----------------------------------------
#  ADD RULES AFTER THIS LINE

