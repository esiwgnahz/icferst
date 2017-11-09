#    Copyright (C) 2006 Imperial College London and others.
#
#    Please see the AUTHORS file in the main source directory for a full list
#    of copyright holders.
#
#    Prof. C Pain
#    Applied Modelling and Computation Group
#    Department of Earth Science and Engineering
#    Imperial College London
#
#    amcgsoftware@imperial.ac.uk
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

PACKAGE_NAME = fluidity
FLUIDITY = $(PACKAGE_NAME)

FC      = mpif90
FCFLAGS = -I../include -J../include -I/usr/include/python2.7 -DHAVE_NUMPY -I/usr/lib/python2.7/dist-packages/numpy/core/include -I/usr/lib/petscdir/3.6.3/include -I/usr/lib/petscdir/3.6.3/linux-gnu-c-opt/include -I/usr/include -I/usr/include/hdf5/openmpi -I/usr/lib/openmpi/include -I/usr/lib/openmpi/include/openmpi/opal/mca/event/libevent2021/libevent -I/usr/lib/openmpi/include/openmpi/opal/mca/event/libevent2021/libevent/include -I/usr/lib/openmpi/include/openmpi -Iinclude/ -DHAVE_PETSC  -I/usr/include/vtk-6.2 -I/usr/include -I/usr/include/jsoncpp -I/usr/include/python2.7 -I/usr/include/freetype2 -I/usr/include/x86_64-linux-gnu/freetype2 -I/usr/include/x86_64-linux-gnu -I/usr/include/hdf5/serial -I/usr/lib/openmpi/include/openmpi/opal/mca/event/libevent2021/libevent -I/usr/lib/openmpi/include/openmpi/opal/mca/event/libevent2021/libevent/include -I/usr/lib/openmpi/include -I/usr/lib/openmpi/include/openmpi -I/usr/include/libxml2 -I/usr/include/tcl   -DHAVE_VTK -fbounds-check -Wall -Wimplicit-interface -Wno-surprising -g -O0 -frecord-marker=4 -DHAVE_NUMPY -I/usr/lib/python2.7/dist-packages/numpy/core/include -fno-realloc-lhs -ffree-line-length-none -ffixed-line-length-none -finit-integer=-66666 -finit-real=nan -I/usr/lib/petscdir/3.6.3/include -I/usr/lib/petscdir/3.6.3/linux-gnu-c-opt/include -I/usr/include -I/usr/include/hdf5/openmpi -I/usr/lib/openmpi/include -I/usr/lib/openmpi/include/openmpi/opal/mca/event/libevent2021/libevent -I/usr/lib/openmpi/include/openmpi/opal/mca/event/libevent2021/libevent/include -I/usr/lib/openmpi/include/openmpi -Iinclude/ -fdefault-real-8 -fdefault-double-8  -I../libwm -I/usr/local/include -I./

MPIF90  = mpif90

CC      = mpicc
CFLAGS  = -I/usr/include/python2.7 -DHAVE_NUMPY -I/usr/lib/python2.7/dist-packages/numpy/core/include -I/usr/lib/petscdir/3.6.3/include -I/usr/lib/petscdir/3.6.3/linux-gnu-c-opt/include -I/usr/include -I/usr/include/hdf5/openmpi -I/usr/lib/openmpi/include -I/usr/lib/openmpi/include/openmpi/opal/mca/event/libevent2021/libevent -I/usr/lib/openmpi/include/openmpi/opal/mca/event/libevent2021/libevent/include -I/usr/lib/openmpi/include/openmpi -Iinclude/ -DHAVE_PETSC  -I/usr/include/vtk-6.2 -I/usr/include -I/usr/include/jsoncpp -I/usr/include/python2.7 -I/usr/include/freetype2 -I/usr/include/x86_64-linux-gnu/freetype2 -I/usr/include/x86_64-linux-gnu -I/usr/include/hdf5/serial -I/usr/lib/openmpi/include/openmpi/opal/mca/event/libevent2021/libevent -I/usr/lib/openmpi/include/openmpi/opal/mca/event/libevent2021/libevent/include -I/usr/lib/openmpi/include -I/usr/lib/openmpi/include/openmpi -I/usr/include/libxml2 -I/usr/include/tcl   -DHAVE_VTK -fbounds-check -Wall -g -O0 -I/usr/include/python2.7 -DHAVE_NUMPY -I/usr/lib/python2.7/dist-packages/numpy/core/include  -I../include -I../libwm -I/usr/local/include

CXX     = mpicxx
CXXFLAGS= -I/usr/include/python2.7 -DHAVE_NUMPY -I/usr/lib/python2.7/dist-packages/numpy/core/include -I/usr/lib/petscdir/3.6.3/include -I/usr/lib/petscdir/3.6.3/linux-gnu-c-opt/include -I/usr/include -I/usr/include/hdf5/openmpi -I/usr/lib/openmpi/include -I/usr/lib/openmpi/include/openmpi/opal/mca/event/libevent2021/libevent -I/usr/lib/openmpi/include/openmpi/opal/mca/event/libevent2021/libevent/include -I/usr/lib/openmpi/include/openmpi -Iinclude/ -DHAVE_PETSC  -I/usr/include/vtk-6.2 -I/usr/include -I/usr/include/jsoncpp -I/usr/include/python2.7 -I/usr/include/freetype2 -I/usr/include/x86_64-linux-gnu/freetype2 -I/usr/include/x86_64-linux-gnu -I/usr/include/hdf5/serial -I/usr/lib/openmpi/include/openmpi/opal/mca/event/libevent2021/libevent -I/usr/lib/openmpi/include/openmpi/opal/mca/event/libevent2021/libevent/include -I/usr/lib/openmpi/include -I/usr/lib/openmpi/include/openmpi -I/usr/include/libxml2 -I/usr/include/tcl   -DHAVE_VTK -fbounds-check -Wall -g -O0 -I/usr/include/python2.7 -DHAVE_NUMPY -I/usr/lib/python2.7/dist-packages/numpy/core/include  -I../include -I../libwm  -I../libvtkfortran/include -I/usr/local/include

LINKER  = mpicxx -rdynamic   

MAKE    = make

AR = ar
ARFLAGS = cr

UNROLL_LOOPS = -funroll-loops

LIB = ../lib/lib$(FLUIDITY).a 

F90LIB = libfemtools.a

LIBS    = -L/usr/lib/ -lnetcdf -L../lib -l$(FLUIDITY) -lmba2d -lzoltan -Wl,-rpath,/usr/lib/petscdir/3.6.3/linux-gnu-c-opt/lib -Wl,-rpath,/usr/lib/petscdir/3.6.3/linux-gnu-c-opt/lib -L/usr/lib/petscdir/3.6.3/linux-gnu-c-opt/lib -lpetsc -Wl,-rpath,/usr/lib/petscdir/3.6.3/linux-gnu-c-opt/lib -lcmumps -ldmumps -lsmumps -lzmumps -lmumps_common -lpord -lumfpack -lklu -lcholmod -lbtf -lccolamd -lcolamd -lcamd -lamd -lsuitesparseconfig -lml -lHYPRE -lscalapack -lexoIIv2for -lexodus -llapack -lblas -lparmetis -Wl,-rpath,/usr/lib -L/usr/lib -lnetcdf -ltriangle -lmetis -lchaco -lhwloc -lctetgen -lhdf5_openmpi -lhdf5_openmpi_hl -lX11 -lptesmumps -lptscotch -lptscotcherr -lscotch -lscotcherr -lm -Wl,-rpath,/usr/lib/openmpi/lib -L/usr/lib/openmpi/lib -Wl,-rpath,/usr/lib/gcc/x86_64-linux-gnu/5 -L/usr/lib/gcc/x86_64-linux-gnu/5 -Wl,-rpath,/usr/lib/x86_64-linux-gnu -L/usr/lib/x86_64-linux-gnu -Wl,-rpath,/lib/x86_64-linux-gnu -L/lib/x86_64-linux-gnu -lmpi_usempif08 -lmpi_usempi_ignore_tkr -lmpi_mpifh -lgfortran -lm -lgfortran -lm -lquadmath -lm -lmpi_cxx -lstdc++ -lrt -lm -lz -Wl,-rpath,/usr/lib/openmpi/lib -L/usr/lib/openmpi/lib -Wl,-rpath,/usr/lib/gcc/x86_64-linux-gnu/5 -L/usr/lib/gcc/x86_64-linux-gnu/5 -Wl,-rpath,/usr/lib/x86_64-linux-gnu -L/usr/lib/x86_64-linux-gnu -Wl,-rpath,/lib/x86_64-linux-gnu -L/lib/x86_64-linux-gnu -Wl,-rpath,/usr/lib/x86_64-linux-gnu -L/usr/lib/x86_64-linux-gnu -ldl -Wl,-rpath,/usr/lib/openmpi/lib -lmpi -lgcc_s -lpthread -ldl -lexoIIv2c -lnetcdf -llapack -ludunits2 -lpthread -lm -lstdc++ -L/usr/lib -lpython2.7 -Xlinker -export-dynamic -Wl,-O0 -Wl,-Bsymbolic-functions -L/usr/lib -lz -lpthread -ldl -lutil -L/usr/lib/gcc/x86_64-linux-gnu/5 -L/usr/lib/gcc/x86_64-linux-gnu/5/../../../x86_64-linux-gnu -L/usr/lib/gcc/x86_64-linux-gnu/5/../../../../lib -L/lib/x86_64-linux-gnu -L/lib/../lib -L/usr/lib/x86_64-linux-gnu -L/usr/lib/../lib -L/usr/lib/gcc/x86_64-linux-gnu/5/../../.. -lgfortran -lm -lquadmath -L/usr/lib/gcc/x86_64-linux-gnu/5 -L/usr/lib/gcc/x86_64-linux-gnu/5/../../../x86_64-linux-gnu -L/usr/lib/gcc/x86_64-linux-gnu/5/../../../../lib -L/lib/x86_64-linux-gnu -L/lib/../lib -L/usr/lib/x86_64-linux-gnu -L/usr/lib/../lib -L/usr/lib/gcc/x86_64-linux-gnu/5/../../.. -lgfortran -lm -lquadmath -L./lib   /usr/lib/x86_64-linux-gnu/libz.so /usr/lib/x86_64-linux-gnu/libjsoncpp.so /usr/lib/x86_64-linux-gnu/libexpat.so -lsqlite3 /usr/lib/x86_64-linux-gnu/libvtkRenderingMatplotlib-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkPythonInterpreter-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libpython2.7.so /usr/lib/x86_64-linux-gnu/libfreetype.so /usr/lib/libvtkWrappingTools-6.2.a /usr/lib/x86_64-linux-gnu/libjpeg.so /usr/lib/x86_64-linux-gnu/libpng.so /usr/lib/x86_64-linux-gnu/libtiff.so /usr/lib/x86_64-linux-gnu/libproj.so /usr/lib/x86_64-linux-gnu/libvtkInteractionImage-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkRenderingImage-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkIOParallel-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkIONetCDF-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libnetcdf_c++.so /usr/lib/x86_64-linux-gnu/libnetcdf.so /usr/lib/x86_64-linux-gnu/hdf5/serial/lib/libhdf5.so -lpthread /usr/lib/x86_64-linux-gnu/libsz.so /usr/lib/x86_64-linux-gnu/libdl.so -lm /usr/lib/x86_64-linux-gnu/hdf5/serial/lib/libhdf5_hl.so /usr/lib/x86_64-linux-gnu/libvtkRenderingParallelLIC-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkRenderingLIC-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkRenderingFreeTypeOpenGL-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkIOParallelXML-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libtheoraenc.so /usr/lib/x86_64-linux-gnu/libtheoradec.so /usr/lib/x86_64-linux-gnu/libogg.so /usr/lib/x86_64-linux-gnu/libvtkIOImport-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkIOODBC-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkIOInfovis-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libxml2.so /usr/lib/x86_64-linux-gnu/libvtkFiltersHyperTree-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkFiltersParallelFlowPaths-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkIOVPIC-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkVPIC-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkIOExport-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkRenderingGL2PS-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkRenderingContextOpenGL-6.2.so.6.2.0 /usr/lib/libgl2ps.so /usr/lib/x86_64-linux-gnu/libvtkIOFFMPEG-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkIOMovie-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkFiltersReebGraph-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkRenderingExternal-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkFiltersParallelStatistics-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkFiltersParallelGeometry-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkWrappingJava-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkIOPLY-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkRenderingVolumeOpenGL-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkImagingStatistics-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkTestingGenericBridge-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkIOParallelExodus-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkFiltersSelection-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkIOMPIImage-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkIOEnSight-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkIOGeoJSON-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkFiltersPython-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkFiltersParallelImaging-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkIOParallelNetCDF-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkIOAMR-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkImagingStencil-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkIOMySQL-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkRenderingFreeTypeFontConfig-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkIOGDAL-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkIOVideo-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkLocalExample-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkTestingIOSQL-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkFiltersSMP-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkIOParallelLSDyna-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkFiltersParallelMPI-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkIOXdmf2-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkImagingMath-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkFiltersVerdict-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkFiltersTexture-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkRenderingParallel-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkTestingRendering-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkFiltersProgrammable-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkIOMINC-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkImagingMorphological-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkDomainsChemistry-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkRenderingLOD-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkViewsContext2D-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkInfovisBoostGraphAlgorithms-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkIOPostgreSQL-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkIOMPIParallel-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkParallelMPI4Py-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkViewsGeovis-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkFiltersGeneric-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkFiltersFlowPaths-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libtheoraenc.so /usr/lib/x86_64-linux-gnu/libtheoradec.so /usr/lib/x86_64-linux-gnu/libogg.so /usr/lib/x86_64-linux-gnu/libvtkIOExodus-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkexoIIc-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libnetcdf_c++.so /usr/lib/x86_64-linux-gnu/libnetcdf.so /usr/lib/x86_64-linux-gnu/libvtkWrappingPython27Core-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkFiltersAMR-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkIOLSDyna-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkxdmf2-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/hdf5/serial/lib/libhdf5.so -lpthread /usr/lib/x86_64-linux-gnu/libsz.so /usr/lib/x86_64-linux-gnu/libdl.so -lm /usr/lib/x86_64-linux-gnu/hdf5/serial/lib/libhdf5_hl.so /usr/lib/x86_64-linux-gnu/libxml2.so /usr/lib/x86_64-linux-gnu/libvtkverdict-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkFiltersParallel-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkRenderingOpenGL-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libGLU.so /usr/lib/x86_64-linux-gnu/libSM.so /usr/lib/x86_64-linux-gnu/libICE.so /usr/lib/x86_64-linux-gnu/libX11.so /usr/lib/x86_64-linux-gnu/libXext.so /usr/lib/x86_64-linux-gnu/libXt.so /usr/lib/x86_64-linux-gnu/libvtkIOSQL-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libpython2.7.so /usr/lib/x86_64-linux-gnu/libvtkParallelMPI-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkParallelCore-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkIOLegacy-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkGeovisCore-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkIOXML-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkIOGeometry-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkIOXMLParser-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libproj.so /usr/lib/x86_64-linux-gnu/libvtkViewsInfovis-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkInfovisLayout-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkViewsCore-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkInteractionWidgets-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkFiltersModeling-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkImagingHybrid-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkIOImage-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkIOCore-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkDICOMParser-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkmetaio-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libz.so /usr/lib/x86_64-linux-gnu/libvtkInteractionStyle-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkFiltersHybrid-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkRenderingAnnotation-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkImagingColor-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkRenderingVolume-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkRenderingLabel-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkChartsCore-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkInfovisCore-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkRenderingContext2D-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkRenderingFreeType-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkRenderingCore-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkFiltersGeometry-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkCommonColor-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkFiltersExtraction-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkftgl-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libfreetype.so /usr/lib/x86_64-linux-gnu/libGL.so /usr/lib/x86_64-linux-gnu/libvtkFiltersImaging-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkFiltersStatistics-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkalglib-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkImagingFourier-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkImagingGeneral-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkImagingSources-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkImagingCore-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkFiltersSources-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkFiltersGeneral-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkFiltersCore-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkCommonExecutionModel-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkCommonComputationalGeometry-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkCommonDataModel-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkCommonMisc-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkCommonTransforms-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkCommonMath-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkCommonSystem-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkCommonCore-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtksys-6.2.so.6.2.0 -ldl -Wl,-rpath,/usr/lib/x86_64-linux-gnu/hdf5/serial/lib   -lblas  -L/usr/lib/gcc/x86_64-linux-gnu/5 -L/usr/lib/gcc/x86_64-linux-gnu/5/../../../x86_64-linux-gnu -L/usr/lib/gcc/x86_64-linux-gnu/5/../../../../lib -L/lib/x86_64-linux-gnu -L/lib/../lib -L/usr/lib/x86_64-linux-gnu -L/usr/lib/../lib -L/usr/lib/gcc/x86_64-linux-gnu/5/../../.. -lgfortran -lm -lquadmath

TESTLIBS = $(shell echo -lmba2d -lzoltan -Wl,-rpath,/usr/lib/petscdir/3.6.3/linux-gnu-c-opt/lib -Wl,-rpath,/usr/lib/petscdir/3.6.3/linux-gnu-c-opt/lib -L/usr/lib/petscdir/3.6.3/linux-gnu-c-opt/lib -lpetsc -Wl,-rpath,/usr/lib/petscdir/3.6.3/linux-gnu-c-opt/lib -lcmumps -ldmumps -lsmumps -lzmumps -lmumps_common -lpord -lumfpack -lklu -lcholmod -lbtf -lccolamd -lcolamd -lcamd -lamd -lsuitesparseconfig -lml -lHYPRE -lscalapack -lexoIIv2for -lexodus -llapack -lblas -lparmetis -Wl,-rpath,/usr/lib -L/usr/lib -lnetcdf -ltriangle -lmetis -lchaco -lhwloc -lctetgen -lhdf5_openmpi -lhdf5_openmpi_hl -lX11 -lptesmumps -lptscotch -lptscotcherr -lscotch -lscotcherr -lm -Wl,-rpath,/usr/lib/openmpi/lib -L/usr/lib/openmpi/lib -Wl,-rpath,/usr/lib/gcc/x86_64-linux-gnu/5 -L/usr/lib/gcc/x86_64-linux-gnu/5 -Wl,-rpath,/usr/lib/x86_64-linux-gnu -L/usr/lib/x86_64-linux-gnu -Wl,-rpath,/lib/x86_64-linux-gnu -L/lib/x86_64-linux-gnu -lmpi_usempif08 -lmpi_usempi_ignore_tkr -lmpi_mpifh -lgfortran -lm -lgfortran -lm -lquadmath -lm -lmpi_cxx -lstdc++ -lrt -lm -lz -Wl,-rpath,/usr/lib/openmpi/lib -L/usr/lib/openmpi/lib -Wl,-rpath,/usr/lib/gcc/x86_64-linux-gnu/5 -L/usr/lib/gcc/x86_64-linux-gnu/5 -Wl,-rpath,/usr/lib/x86_64-linux-gnu -L/usr/lib/x86_64-linux-gnu -Wl,-rpath,/lib/x86_64-linux-gnu -L/lib/x86_64-linux-gnu -Wl,-rpath,/usr/lib/x86_64-linux-gnu -L/usr/lib/x86_64-linux-gnu -ldl -Wl,-rpath,/usr/lib/openmpi/lib -lmpi -lgcc_s -lpthread -ldl -lexoIIv2c -lnetcdf -llapack -ludunits2 -lpthread -lm -lstdc++ -L/usr/lib -lpython2.7 -Xlinker -export-dynamic -Wl,-O0 -Wl,-Bsymbolic-functions -L/usr/lib -lz -lpthread -ldl -lutil -L/usr/lib/gcc/x86_64-linux-gnu/5 -L/usr/lib/gcc/x86_64-linux-gnu/5/../../../x86_64-linux-gnu -L/usr/lib/gcc/x86_64-linux-gnu/5/../../../../lib -L/lib/x86_64-linux-gnu -L/lib/../lib -L/usr/lib/x86_64-linux-gnu -L/usr/lib/../lib -L/usr/lib/gcc/x86_64-linux-gnu/5/../../.. -lgfortran -lm -lquadmath -L/usr/lib/gcc/x86_64-linux-gnu/5 -L/usr/lib/gcc/x86_64-linux-gnu/5/../../../x86_64-linux-gnu -L/usr/lib/gcc/x86_64-linux-gnu/5/../../../../lib -L/lib/x86_64-linux-gnu -L/lib/../lib -L/usr/lib/x86_64-linux-gnu -L/usr/lib/../lib -L/usr/lib/gcc/x86_64-linux-gnu/5/../../.. -lgfortran -lm -lquadmath -L./lib   /usr/lib/x86_64-linux-gnu/libz.so /usr/lib/x86_64-linux-gnu/libjsoncpp.so /usr/lib/x86_64-linux-gnu/libexpat.so -lsqlite3 /usr/lib/x86_64-linux-gnu/libvtkRenderingMatplotlib-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkPythonInterpreter-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libpython2.7.so /usr/lib/x86_64-linux-gnu/libfreetype.so /usr/lib/libvtkWrappingTools-6.2.a /usr/lib/x86_64-linux-gnu/libjpeg.so /usr/lib/x86_64-linux-gnu/libpng.so /usr/lib/x86_64-linux-gnu/libtiff.so /usr/lib/x86_64-linux-gnu/libproj.so /usr/lib/x86_64-linux-gnu/libvtkInteractionImage-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkRenderingImage-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkIOParallel-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkIONetCDF-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libnetcdf_c++.so /usr/lib/x86_64-linux-gnu/libnetcdf.so /usr/lib/x86_64-linux-gnu/hdf5/serial/lib/libhdf5.so -lpthread /usr/lib/x86_64-linux-gnu/libsz.so /usr/lib/x86_64-linux-gnu/libdl.so -lm /usr/lib/x86_64-linux-gnu/hdf5/serial/lib/libhdf5_hl.so /usr/lib/x86_64-linux-gnu/libvtkRenderingParallelLIC-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkRenderingLIC-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkRenderingFreeTypeOpenGL-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkIOParallelXML-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libtheoraenc.so /usr/lib/x86_64-linux-gnu/libtheoradec.so /usr/lib/x86_64-linux-gnu/libogg.so /usr/lib/x86_64-linux-gnu/libvtkIOImport-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkIOODBC-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkIOInfovis-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libxml2.so /usr/lib/x86_64-linux-gnu/libvtkFiltersHyperTree-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkFiltersParallelFlowPaths-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkIOVPIC-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkVPIC-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkIOExport-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkRenderingGL2PS-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkRenderingContextOpenGL-6.2.so.6.2.0 /usr/lib/libgl2ps.so /usr/lib/x86_64-linux-gnu/libvtkIOFFMPEG-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkIOMovie-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkFiltersReebGraph-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkRenderingExternal-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkFiltersParallelStatistics-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkFiltersParallelGeometry-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkWrappingJava-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkIOPLY-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkRenderingVolumeOpenGL-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkImagingStatistics-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkTestingGenericBridge-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkIOParallelExodus-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkFiltersSelection-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkIOMPIImage-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkIOEnSight-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkIOGeoJSON-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkFiltersPython-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkFiltersParallelImaging-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkIOParallelNetCDF-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkIOAMR-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkImagingStencil-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkIOMySQL-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkRenderingFreeTypeFontConfig-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkIOGDAL-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkIOVideo-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkLocalExample-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkTestingIOSQL-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkFiltersSMP-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkIOParallelLSDyna-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkFiltersParallelMPI-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkIOXdmf2-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkImagingMath-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkFiltersVerdict-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkFiltersTexture-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkRenderingParallel-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkTestingRendering-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkFiltersProgrammable-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkIOMINC-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkImagingMorphological-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkDomainsChemistry-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkRenderingLOD-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkViewsContext2D-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkInfovisBoostGraphAlgorithms-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkIOPostgreSQL-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkIOMPIParallel-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkParallelMPI4Py-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkViewsGeovis-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkFiltersGeneric-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkFiltersFlowPaths-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libtheoraenc.so /usr/lib/x86_64-linux-gnu/libtheoradec.so /usr/lib/x86_64-linux-gnu/libogg.so /usr/lib/x86_64-linux-gnu/libvtkIOExodus-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkexoIIc-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libnetcdf_c++.so /usr/lib/x86_64-linux-gnu/libnetcdf.so /usr/lib/x86_64-linux-gnu/libvtkWrappingPython27Core-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkFiltersAMR-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkIOLSDyna-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkxdmf2-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/hdf5/serial/lib/libhdf5.so -lpthread /usr/lib/x86_64-linux-gnu/libsz.so /usr/lib/x86_64-linux-gnu/libdl.so -lm /usr/lib/x86_64-linux-gnu/hdf5/serial/lib/libhdf5_hl.so /usr/lib/x86_64-linux-gnu/libxml2.so /usr/lib/x86_64-linux-gnu/libvtkverdict-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkFiltersParallel-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkRenderingOpenGL-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libGLU.so /usr/lib/x86_64-linux-gnu/libSM.so /usr/lib/x86_64-linux-gnu/libICE.so /usr/lib/x86_64-linux-gnu/libX11.so /usr/lib/x86_64-linux-gnu/libXext.so /usr/lib/x86_64-linux-gnu/libXt.so /usr/lib/x86_64-linux-gnu/libvtkIOSQL-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libpython2.7.so /usr/lib/x86_64-linux-gnu/libvtkParallelMPI-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkParallelCore-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkIOLegacy-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkGeovisCore-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkIOXML-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkIOGeometry-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkIOXMLParser-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libproj.so /usr/lib/x86_64-linux-gnu/libvtkViewsInfovis-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkInfovisLayout-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkViewsCore-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkInteractionWidgets-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkFiltersModeling-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkImagingHybrid-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkIOImage-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkIOCore-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkDICOMParser-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkmetaio-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libz.so /usr/lib/x86_64-linux-gnu/libvtkInteractionStyle-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkFiltersHybrid-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkRenderingAnnotation-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkImagingColor-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkRenderingVolume-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkRenderingLabel-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkChartsCore-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkInfovisCore-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkRenderingContext2D-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkRenderingFreeType-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkRenderingCore-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkFiltersGeometry-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkCommonColor-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkFiltersExtraction-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkftgl-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libfreetype.so /usr/lib/x86_64-linux-gnu/libGL.so /usr/lib/x86_64-linux-gnu/libvtkFiltersImaging-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkFiltersStatistics-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkalglib-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkImagingFourier-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkImagingGeneral-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkImagingSources-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkImagingCore-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkFiltersSources-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkFiltersGeneral-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkFiltersCore-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkCommonExecutionModel-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkCommonComputationalGeometry-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkCommonDataModel-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkCommonMisc-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkCommonTransforms-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkCommonMath-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkCommonSystem-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkCommonCore-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtksys-6.2.so.6.2.0 -ldl -Wl,-rpath,/usr/lib/x86_64-linux-gnu/hdf5/serial/lib   | sed 's@./lib/lib\([a-z]*\)\.a@-l\1@g')

OBJS = Dgtools.o Coordinates.o EventCounter.o \
  Elements.o Sparse_Tools.o Quadrature.o Quadrature_Test.o Futils.o		\
  Polynomials.o Adjacency_Lists.o Element_Numbering.o Global_Numbering.o \
  Shape_Functions.o Shape_Functions_Test.o Signals.o Signal_Vars.o signal_handlers.o		\
  Global_Parameters.o Timers.o Transform_elements.o VTK_interfaces.o \
  Fields.o FETools.o FEFields.o Vector_Tools.o Read_Triangle.o \
  Timers.o Transform_elements.o Petsc_Tools.o Solvers.o Linked_Lists.o	\
  Sparsity_Patterns.o Sparsity_Patterns_Meshes.o State.o Tensors.o \
  Superconvergence.o Unittest_tools.o Fields_Data_Types.o Multigrid.o	\
  ieee_arithmetic_dummy.o ieee_arithmetic_C99.o Diagnostic_variables.o	\
  Diagnostic_Fields.o SampleNetCDF_fortran.o \
  AuxilaryOptions.o MeshDiagnostics.o VTK_interfaces.o Surface_Labels.o	\
  ISCopyIndices.o Colouring.o \
  Field_derivatives.o Node_boundary.o Parallel_fields.o \
  Vector_set.o Element_set.o vecset.o intvecset.o eleset.o \
  Matrix_Norms.o embed_python.o Embed_Python_Fortran.o \
  external_function.o Reference_Counting.o \
  Tokenize.o Boundary_Conditions.o Write_Triangle.o \
  tictoc.o \
  CVTools.o CV_Fields.o CV_Face_Values.o CV_Upwind_Values.o CV_Shape_Functions.o CV_Faces.o \
  CV_Options.o Metric_tools.o \
  Merge_tensors.o Write_State.o Field_Options.o \
  Fields_Base.o Fields_Allocates.o Fields_Calculations.o Fields_Manipulation.o \
  Sparse_Matrices_Fields.o Unittest_Tools_Cpp.o Adaptive_Timestepping.o \
  Checkpoint.o Surface_Integrals.o\
  python_state.o python_statec.o Dynamic_Bin_Sort.o \
  Supermesh.o Supermesh_Assembly.o Conservative_interpolation.o \
  Interpolation.o Pseudo_Consistent_Interpolation.o Pseudo_2D.o DG_interpolation.o \
  Halo_Data_Types.o Halos.o Halos_Allocates.o Halos_Base.o \
  Halos_Communications.o Halos_Debug.o Halos_Derivation.o Halos_IO.o \
  Halos_Numbering.o Halos_Ownership.o Halos_Registration.o Halos_Repair.o \
  qsortd.o Element_Intersection.o Intersection_finder.o tri_predicate.o \
  tet_predicate.o Lagrangian_Remap.o \
  Detector_Data_Types.o Detector_Tools.o \
  Detector_Parallel.o Detector_Move_Lagrangian.o \
  Picker_Data_Types.o Pickers.o Pickers_Allocates.o \
  Pickers_Base.o Pickers_Deallocates.o Pickers_Inquire.o Smoothing_module.o \
  vtk_read_files.o State_Fields.o Unify_meshes.o Adaptive_interpolation.o \
  Wandzura_Quadrature.o Grundmann_Moeller_Quadrature.o Bound_field.o \
  Halos_Diagnostics.o Mixing_Statistics.o projections.o Memory_Diagnostics.o \
  Sparse_Tools_Petsc.o C_Interfaces.o C_Interfaces_Fortran.o Tetrahedron_intersection.o \
  Node_Owner_Finder.o Node_Owner_Finder_Fortran.o Node_Ownership.o \
  Data_structures.o Data_structures_C.o Integer_set.o Integer_hash_table.o \
  CGAL_Tools_C.o CGAL_Tools.o \
  Rotated_Boundary_Conditions.o MPI_Interfaces.o Parallel_Tools.o \
  Fields_Halos.o Profiler.o Profiler_Fortran.o Streamfunction.o \
  GMSH_Common.o Read_GMSH.o Write_GMSH.o \
  Exodusii_C_Interface.o Exodusii_F_Interface.o Exodusii_Common.o Read_Exodusii.o \
  Mesh_Files.o Vertical_Extrapolation.o


# objects to be included in libfemtools:
F90LIB_OBJS := ../debug/*.o ../libwm/*.o  \
  $(OBJS)

.SUFFIXES: .F90 .cpp .c .o .a

# cancel implicit rule that tries to make .o from .mod with m2c:
%.o: %.mod

.F90.o:
	@echo "        FC $<"
	$(FC) $(FCFLAGS)  $(GENFLAGS) -c $< 
.c.o:
	@echo "        CC $<"
	$(CC) $(CFLAGS) -c $<
.cpp.o:
	@echo "        CXX $<"
	$(CXX) $(CXXFLAGS) -c $<

$(LIB): $(OBJS)
	@mkdir -p ../lib

default: $(LIB)

$(F90LIB): $(F90LIB_OBJS)
	@mkdir -p ../lib
	$(AR) $(ARFLAGS) $@ $(F90LIB_OBJS)

libfemtools: $(F90LIB)

clean:
	rm -f *.o *.d *.mod Reference_count_*.F90 $(F90LIB)

../include/version.h: version-info

version-info: 
	@$(MAKE) -C .. include/version.h

.PHONY: version-info

Reference_count_%.F90: Reference_count_interface_%.F90
	@true

Reference_count_interface_%.F90: Refcount_templates.F90 Refcount_interface_templates.F90
	@sed 's/REFCOUNT_TYPE/$*/' Refcount_templates.F90 > Reference_count_$*.F90
	@sed 's/REFCOUNT_TYPE/$*/' Refcount_interface_templates.F90 > Reference_count_interface_$*.F90

test_projections: projections.cpp
	$(CXX) $(CXXFLAGS) -DPROJECTIONS_UNIT_TEST -o $@ $^ $(LIBS)

Conservative_interpolation.o: Conservative_interpolation.F90 
	@echo "        FC $<"
	$(FC) $(FCFLAGS) $(UNROLL_LOOPS) $(GENFLAGS) -c $< || (rm $(LIB) && false)

FETools.o: FETools.F90 
	@echo "        FC $<"
	$(FC) $(FCFLAGS) $(UNROLL_LOOPS) $(GENFLAGS) -c $< || (rm $(LIB) && false)

# The refcount template dependencies are not actually needed for
# Reference_counting.o but they are needed by everything which depends on
# Reference_counting.o
Reference_Counting.o: \
  Refcount_templates.F90 Refcount_interface_templates.F90

test_element_numbering:test_element_numbering.F90 
	$(FC) $(FCFLAGS) -o $@ $^

testshapefunctions:testshapefunctions.F90 
	$(FC) $(FCFLAGS) -o $@ $^

testvectortools:testvectortools.F90 
	$(FC) $(FCFLAGS) -o $@ $^ $(LIBS)

test_laplacian:test_laplacian.F90 
	$(FC) $(FCFLAGS) -o $@ $^ $(LIBS)

include Makefile.dependencies
