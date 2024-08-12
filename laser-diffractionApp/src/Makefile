TOP=../..

include $(TOP)/configure/CONFIG
#----------------------------------------
#  ADD MACRO DEFINITIONS AFTER THIS LINE
#=============================

#=============================
# Build the IOC application

PROD_IOC = laser-diffraction
# laser-diffraction.dbd will be created and installed
DBD += laser-diffraction.dbd

# laser-diffraction.dbd will be made up from these files:
laser-diffraction_DBD += base.dbd

# Include dbd files from all support applications:
#laser-diffraction_DBD += xxx.dbd

# Add all the support libraries needed by this IOC
#laser-diffraction_LIBS += xxx

# laser-diffraction_registerRecordDeviceDriver.cpp derives from laser-diffraction.dbd
laser-diffraction_SRCS += laser-diffraction_registerRecordDeviceDriver.cpp

# Build the main IOC entry point on workstation OSs.
laser-diffraction_SRCS_DEFAULT += laser-diffractionMain.cpp
laser-diffraction_SRCS_vxWorks += -nil-

# Add support from base/src/vxWorks if needed
#laser-diffraction_OBJS_vxWorks += $(EPICS_BASE_BIN)/vxComLibrary

# Finally link to the EPICS Base libraries
laser-diffraction_LIBS += $(EPICS_BASE_IOC_LIBS)

#===========================

include $(TOP)/configure/RULES
#----------------------------------------
#  ADD RULES AFTER THIS LINE

