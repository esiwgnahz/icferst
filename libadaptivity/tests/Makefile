#    Copyright (C) 2009 Imperial College London and others.
#
#    Please see the AUTHORS file in the main source directory for a full list
#    of copyright holders.
#
#    Gerard Gorman
#    Applied Modelling and Computation Group
#    Department of Earth Science and Engineering
#    Imperial College London
#
#    g.gorman@imperial.ac.uk
#
#    This library is free software; you can redistribute it and/or
#    modify it under the terms of the GNU Lesser General Public
#    License as published by the Free Software Foundation,
#    version 2.1 of the License.
#
#    This library is distributed in the hope that it will be useful,
#    but WITHOUT ANY WARRANTY; without even the implied warranty of
#    MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the GNU
#    Lesser General Public License for more details.
#
#    You should have received a copy of the GNU Lesser General Public
#    License along with this library; if not, write to the Free Software
#    Foundation, Inc., 59 Temple Place, Suite 330, Boston, MA  02111-1307
#    USA
SHELL = /bin/bash

CPPFLAGS =  -I/usr/include/vtk-6.2 -I/usr/include -I/usr/include/jsoncpp -I/usr/include/python2.7 -I/usr/include/freetype2 -I/usr/include/x86_64-linux-gnu/freetype2 -I/usr/include/x86_64-linux-gnu -I/usr/include/hdf5/serial -I/usr/lib/openmpi/include/openmpi/opal/mca/event/libevent2021/libevent -I/usr/lib/openmpi/include/openmpi/opal/mca/event/libevent2021/libevent/include -I/usr/lib/openmpi/include -I/usr/lib/openmpi/include/openmpi -I/usr/include/libxml2 -I/usr/include/tcl   -DHAVE_VTK -I../load_balance/include \
	-I../adapt3d/include -I../metric_field/include -I../include

F77     = mpif90
FFLAGS  = $(CPPFLAGS) -ffast-math -frecord-marker=4    -ffree-line-length-none -ffixed-line-length-none  -O3 -fdefault-real-8

FC      = mpif90
FCFLAGS = $(CPPFLAGS) -ffast-math -frecord-marker=4    -ffree-line-length-none -ffixed-line-length-none  -O3 -fdefault-real-8

CC      = mpicc
CCFLAGS = $(CPPFLAGS) @CCFLAGS@

CXX     = mpicxx
CXXFLAGS= $(CPPFLAGS)   -O3 

LINKER  = mpicxx
LDFLAGS =   
 
LIBS    = ../lib/libadaptivity.a  -llapack -lblas -lpthread -lm -lstdc++       /usr/lib/x86_64-linux-gnu/libz.so /usr/lib/x86_64-linux-gnu/libjsoncpp.so /usr/lib/x86_64-linux-gnu/libexpat.so -lsqlite3 /usr/lib/x86_64-linux-gnu/libvtkRenderingMatplotlib-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkPythonInterpreter-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libpython2.7.so /usr/lib/x86_64-linux-gnu/libfreetype.so /usr/lib/libvtkWrappingTools-6.2.a /usr/lib/x86_64-linux-gnu/libjpeg.so /usr/lib/x86_64-linux-gnu/libpng.so /usr/lib/x86_64-linux-gnu/libtiff.so /usr/lib/x86_64-linux-gnu/libproj.so /usr/lib/x86_64-linux-gnu/libvtkInteractionImage-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkRenderingImage-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkIOParallel-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkIONetCDF-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libnetcdf_c++.so /usr/lib/x86_64-linux-gnu/libnetcdf.so /usr/lib/x86_64-linux-gnu/hdf5/serial/lib/libhdf5.so -lpthread /usr/lib/x86_64-linux-gnu/libsz.so /usr/lib/x86_64-linux-gnu/libdl.so -lm /usr/lib/x86_64-linux-gnu/hdf5/serial/lib/libhdf5_hl.so /usr/lib/x86_64-linux-gnu/libvtkRenderingParallelLIC-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkRenderingLIC-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkRenderingFreeTypeOpenGL-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkIOParallelXML-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libtheoraenc.so /usr/lib/x86_64-linux-gnu/libtheoradec.so /usr/lib/x86_64-linux-gnu/libogg.so /usr/lib/x86_64-linux-gnu/libvtkIOImport-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkIOODBC-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkIOInfovis-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libxml2.so /usr/lib/x86_64-linux-gnu/libvtkFiltersHyperTree-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkFiltersParallelFlowPaths-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkIOVPIC-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkVPIC-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkIOExport-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkRenderingGL2PS-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkRenderingContextOpenGL-6.2.so.6.2.0 /usr/lib/libgl2ps.so /usr/lib/x86_64-linux-gnu/libvtkIOFFMPEG-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkIOMovie-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkFiltersReebGraph-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkRenderingExternal-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkFiltersParallelStatistics-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkFiltersParallelGeometry-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkWrappingJava-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkIOPLY-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkRenderingVolumeOpenGL-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkImagingStatistics-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkTestingGenericBridge-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkIOParallelExodus-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkFiltersSelection-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkIOMPIImage-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkIOEnSight-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkIOGeoJSON-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkFiltersPython-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkFiltersParallelImaging-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkIOParallelNetCDF-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkIOAMR-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkImagingStencil-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkIOMySQL-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkRenderingFreeTypeFontConfig-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkIOGDAL-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkIOVideo-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkLocalExample-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkTestingIOSQL-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkFiltersSMP-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkIOParallelLSDyna-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkFiltersParallelMPI-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkIOXdmf2-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkImagingMath-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkFiltersVerdict-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkFiltersTexture-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkRenderingParallel-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkTestingRendering-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkFiltersProgrammable-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkIOMINC-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkImagingMorphological-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkDomainsChemistry-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkRenderingLOD-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkViewsContext2D-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkInfovisBoostGraphAlgorithms-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkIOPostgreSQL-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkIOMPIParallel-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkParallelMPI4Py-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkViewsGeovis-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkFiltersGeneric-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkFiltersFlowPaths-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libtheoraenc.so /usr/lib/x86_64-linux-gnu/libtheoradec.so /usr/lib/x86_64-linux-gnu/libogg.so /usr/lib/x86_64-linux-gnu/libvtkIOExodus-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkexoIIc-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libnetcdf_c++.so /usr/lib/x86_64-linux-gnu/libnetcdf.so /usr/lib/x86_64-linux-gnu/libvtkWrappingPython27Core-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkFiltersAMR-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkIOLSDyna-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkxdmf2-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/hdf5/serial/lib/libhdf5.so -lpthread /usr/lib/x86_64-linux-gnu/libsz.so /usr/lib/x86_64-linux-gnu/libdl.so -lm /usr/lib/x86_64-linux-gnu/hdf5/serial/lib/libhdf5_hl.so /usr/lib/x86_64-linux-gnu/libxml2.so /usr/lib/x86_64-linux-gnu/libvtkverdict-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkFiltersParallel-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkRenderingOpenGL-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libGLU.so /usr/lib/x86_64-linux-gnu/libSM.so /usr/lib/x86_64-linux-gnu/libICE.so /usr/lib/x86_64-linux-gnu/libX11.so /usr/lib/x86_64-linux-gnu/libXext.so /usr/lib/x86_64-linux-gnu/libXt.so /usr/lib/x86_64-linux-gnu/libvtkIOSQL-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libpython2.7.so /usr/lib/x86_64-linux-gnu/libvtkParallelMPI-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkParallelCore-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkIOLegacy-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkGeovisCore-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkIOXML-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkIOGeometry-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkIOXMLParser-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libproj.so /usr/lib/x86_64-linux-gnu/libvtkViewsInfovis-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkInfovisLayout-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkViewsCore-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkInteractionWidgets-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkFiltersModeling-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkImagingHybrid-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkIOImage-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkIOCore-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkDICOMParser-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkmetaio-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libz.so /usr/lib/x86_64-linux-gnu/libvtkInteractionStyle-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkFiltersHybrid-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkRenderingAnnotation-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkImagingColor-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkRenderingVolume-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkRenderingLabel-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkChartsCore-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkInfovisCore-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkRenderingContext2D-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkRenderingFreeType-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkRenderingCore-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkFiltersGeometry-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkCommonColor-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkFiltersExtraction-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkftgl-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libfreetype.so /usr/lib/x86_64-linux-gnu/libGL.so /usr/lib/x86_64-linux-gnu/libvtkFiltersImaging-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkFiltersStatistics-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkalglib-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkImagingFourier-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkImagingGeneral-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkImagingSources-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkImagingCore-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkFiltersSources-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkFiltersGeneral-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkFiltersCore-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkCommonExecutionModel-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkCommonComputationalGeometry-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkCommonDataModel-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkCommonMisc-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkCommonTransforms-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkCommonMath-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkCommonSystem-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkCommonCore-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtksys-6.2.so.6.2.0 -ldl -Wl,-rpath,/usr/lib/x86_64-linux-gnu/hdf5/serial/lib   -L/usr/lib/gcc/x86_64-linux-gnu/5 -L/usr/lib/gcc/x86_64-linux-gnu/5/../../../x86_64-linux-gnu -L/usr/lib/gcc/x86_64-linux-gnu/5/../../../../lib -L/lib/x86_64-linux-gnu -L/lib/../lib -L/usr/lib/x86_64-linux-gnu -L/usr/lib/../lib -L/usr/lib/gcc/x86_64-linux-gnu/5/../../.. -lgfortran -lm -lquadmath -L/usr/lib/gcc/x86_64-linux-gnu/5 -L/usr/lib/gcc/x86_64-linux-gnu/5/../../../x86_64-linux-gnu -L/usr/lib/gcc/x86_64-linux-gnu/5/../../../../lib -L/lib/x86_64-linux-gnu -L/lib/../lib -L/usr/lib/x86_64-linux-gnu -L/usr/lib/../lib -L/usr/lib/gcc/x86_64-linux-gnu/5/../../.. -lgfortran -lm -lquadmath -L./lib -L/usr/lib/gcc/x86_64-linux-gnu/5 -L/usr/lib/gcc/x86_64-linux-gnu/5/../../../x86_64-linux-gnu -L/usr/lib/gcc/x86_64-linux-gnu/5/../../../../lib -L/lib/x86_64-linux-gnu -L/lib/../lib -L/usr/lib/x86_64-linux-gnu -L/usr/lib/../lib -L/usr/lib/gcc/x86_64-linux-gnu/5/../../.. -lgfortran -lm -lquadmath

MAKE    = make
INSTALL = /usr/bin/install -c

.SUFFIXES: .F .F90 .c .o .a

.F.o:
	$(F77) $(FFLAGS) -c $<

.F90.o:
	$(FC) $(FCFLAGS) -c $<

.c.o:
	$(CC) $(CCFLAGS) -c $<

.cxx.o:
	$(CXX) $(CXXFLAGS) -c $<

OBJS = test_adapt_full.o test_metrictensor.o
TESTS = test_adapt_full test_metrictensor

default: $(OBJS)
	$(CXX) $(LDFLAGS) -o test_adapt_full test_adapt_full.o $(LIBS)
	$(CXX) $(LDFLAGS) -o test_metrictensor test_metrictensor.o $(LIBS)

clean:
	rm -f *.o $(TESTS)
