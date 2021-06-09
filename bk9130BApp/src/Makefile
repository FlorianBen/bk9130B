TOP=../..

include $(TOP)/configure/CONFIG
#----------------------------------------
#  ADD MACRO DEFINITIONS BELOW HERE
# Build the IOC application
PROD_IOC = bk9130B

# bk9130B.dbd will be created and installed
DBD += bk9130B.dbd

# bk9130B.dbd will include these files:
bk9130B_DBD += base.dbd
bk9130B_DBD += calcSupport.dbd
bk9130B_DBD += stream.dbd
bk9130B_DBD += asyn.dbd
bk9130B_DBD += drvAsynSerialPort.dbd
bk9130B_DBD += drvAsynIPPort.dbd
bk9130B_DBD += drvAsynUSBTMC.dbd

# Link in the code from our support library
bk9130B_LIBS += calc stream asyn

# bk9130B_registerRecordDeviceDriver.cpp derives from bk9130B.dbd
bk9130B_SRCS += bk9130B_registerRecordDeviceDriver.cpp

# Build the main IOC entry point where needed
bk9130B_SRCS_DEFAULT += bk9130BMain.cpp
bk9130B_SRCS_vxWorks += -nil-

# Finally link IOC to the EPICS Base libraries
bk9130B_LIBS += $(EPICS_BASE_IOC_LIBS)
bk9130B_SYS_LIBS += usb-1.0

include $(TOP)/configure/RULES
#----------------------------------------
#  ADD EXTRA GNUMAKE RULES BELOW HERE
