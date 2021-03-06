XERCES_LIBS = -l$(LIB_XERCES)

MESO_LIBS = ../../src/mesosim/libmesosim.a

if WITH_GUI
GUI_TESTS = ./utils/foxtools/FXWorkerThreadTest.o
endif


if WITH_GTEST
bin_PROGRAMS = sumo-unittest

sumo_unittest_SOURCES = unittest_main.cpp

sumo_unittest_LDFLAGS = $(GTEST_LDFLAGS) $(GDAL_LDFLAGS) $(PROJ_LDFLAGS)

sumo_unittest_LDADD   = \
./utils/common/StringUtilsTest.o \
./utils/common/StringTokenizerTest.o \
./utils/common/RandHelperTest.o \
./utils/common/RGBColorTest.o \
./utils/common/ValueTimeLineTest.o \
./utils/geom/BoundaryTest.o \
./utils/geom/PositionVectorTest.o \
./utils/geom/GeomHelperTest.o \
./utils/geom/GeoConvHelperTest.o \
./netbuild/NBHeightMapperTest.o \
./netbuild/NBTrafficLightLogicTest.o \
./microsim/MSCFModelTest.o \
./microsim/MSCFModel_IDMTest.o \
./microsim/MSEventControlTest.o \
$(GUI_TESTS) \
../../src/traci-server/libtraciserver.a \
../../src/libsumo/libsumostatic.a \
../../src/traci-server/TraCIServer.o \
../../src/netbuild/libnetbuild.a \
../../src/netload/libnetload.a \
../../src/microsim/libmicrosim.a \
../../src/microsim/MSJunctionLogic.o \
../../src/microsim/MSNoLogicJunction.o \
../../src/microsim/devices/libmicrosimdevs.a \
../../src/microsim/trigger/libmicrosimtrigger.a \
../../src/microsim/cfmodels/libmicrosimcfmodels.a \
../../src/microsim/lcmodels/libmicrosimlcmodels.a \
../../src/microsim/pedestrians/libmicrosimpeds.a \
../../src/microsim/output/libmicrosimoutput.a \
../../src/microsim/MSMoveReminder.o \
../../src/microsim/actions/libmsactions.a \
../../src/microsim/traffic_lights/libmicrosimtls.a \
$(MESO_LIBS) \
../../src/utils/geom/libgeom.a \
../../src/utils/shapes/libshapes.a \
../../src/utils/emissions/libemissions.a \
../../src/utils/xml/libxml.a \
../../src/utils/distribution/libdistribution.a \
../../src/utils/vehicle/libvehicle.a \
../../src/utils/common/libcommon.a \
../../src/utils/options/liboptions.a \
../../src/utils/iodevices/libiodevices.a \
../../src/utils/common/FileHelpers.o \
../../src/foreign/PHEMlight/cpp/libphemlight.a \
../../src/foreign/tcpip/libtcpip.a \
$(PYTHON_LIBS) \
$(XERCES_LIBS) \
$(FOX_LDFLAGS)

SUBDIRS = utils microsim netbuild
endif
