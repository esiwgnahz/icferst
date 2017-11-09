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
FCFLAGS = -I../include -I/usr/include -I/usr/include/python2.7 -DHAVE_NUMPY -I/usr/lib/python2.7/dist-packages/numpy/core/include -I/usr/lib/petscdir/3.6.3/include -I/usr/lib/petscdir/3.6.3/linux-gnu-c-opt/include -I/usr/include -I/usr/include/hdf5/openmpi -I/usr/lib/openmpi/include -I/usr/lib/openmpi/include/openmpi/opal/mca/event/libevent2021/libevent -I/usr/lib/openmpi/include/openmpi/opal/mca/event/libevent2021/libevent/include -I/usr/lib/openmpi/include/openmpi -Iinclude/ -DHAVE_PETSC  -I/usr/include/vtk-6.2 -I/usr/include -I/usr/include/jsoncpp -I/usr/include/python2.7 -I/usr/include/freetype2 -I/usr/include/x86_64-linux-gnu/freetype2 -I/usr/include/x86_64-linux-gnu -I/usr/include/hdf5/serial -I/usr/lib/openmpi/include/openmpi/opal/mca/event/libevent2021/libevent -I/usr/lib/openmpi/include/openmpi/opal/mca/event/libevent2021/libevent/include -I/usr/lib/openmpi/include -I/usr/lib/openmpi/include/openmpi -I/usr/include/libxml2 -I/usr/include/tcl   -DHAVE_VTK -fbounds-check -Wall -Wimplicit-interface -Wno-surprising -g -O0 -frecord-marker=4 -DHAVE_NUMPY -I/usr/lib/python2.7/dist-packages/numpy/core/include -fno-realloc-lhs -ffree-line-length-none -ffixed-line-length-none -finit-integer=-66666 -finit-real=nan -I/usr/lib/petscdir/3.6.3/include -I/usr/lib/petscdir/3.6.3/linux-gnu-c-opt/include -I/usr/include -I/usr/include/hdf5/openmpi -I/usr/lib/openmpi/include -I/usr/lib/openmpi/include/openmpi/opal/mca/event/libevent2021/libevent -I/usr/lib/openmpi/include/openmpi/opal/mca/event/libevent2021/libevent/include -I/usr/lib/openmpi/include/openmpi -Iinclude/ -fdefault-real-8 -fdefault-double-8

CC  = mpicc
CFLAGS  = -fbounds-check -Wall -g -O0 -I/usr/include/python2.7 -DHAVE_NUMPY -I/usr/lib/python2.7/dist-packages/numpy/core/include  -I../include

CXX = mpicxx
CXXFLAGS= -I/usr/include/python2.7 -DHAVE_NUMPY -I/usr/lib/python2.7/dist-packages/numpy/core/include -I/usr/lib/petscdir/3.6.3/include -I/usr/lib/petscdir/3.6.3/linux-gnu-c-opt/include -I/usr/include -I/usr/include/hdf5/openmpi -I/usr/lib/openmpi/include -I/usr/lib/openmpi/include/openmpi/opal/mca/event/libevent2021/libevent -I/usr/lib/openmpi/include/openmpi/opal/mca/event/libevent2021/libevent/include -I/usr/lib/openmpi/include/openmpi -Iinclude/ -DHAVE_PETSC  -I/usr/include/vtk-6.2 -I/usr/include -I/usr/include/jsoncpp -I/usr/include/python2.7 -I/usr/include/freetype2 -I/usr/include/x86_64-linux-gnu/freetype2 -I/usr/include/x86_64-linux-gnu -I/usr/include/hdf5/serial -I/usr/lib/openmpi/include/openmpi/opal/mca/event/libevent2021/libevent -I/usr/lib/openmpi/include/openmpi/opal/mca/event/libevent2021/libevent/include -I/usr/lib/openmpi/include -I/usr/lib/openmpi/include/openmpi -I/usr/include/libxml2 -I/usr/include/tcl   -DHAVE_VTK -fbounds-check -Wall -g -O0 -I/usr/include/python2.7 -DHAVE_NUMPY -I/usr/lib/python2.7/dist-packages/numpy/core/include  -I../include

LINKER = mpicxx -rdynamic   

FLLINKER = mpif90 -rdynamic    $(FCFLAGS)

LIBS = -L../lib ./lib/libadaptivity.a ./lib/libspatialindex.a ./lib/libspud.a ./lib/libvtkfortran.a ./lib/libjudy.a -lmba2d -lzoltan -Wl,-rpath,/usr/lib/petscdir/3.6.3/linux-gnu-c-opt/lib -Wl,-rpath,/usr/lib/petscdir/3.6.3/linux-gnu-c-opt/lib -L/usr/lib/petscdir/3.6.3/linux-gnu-c-opt/lib -lpetsc -Wl,-rpath,/usr/lib/petscdir/3.6.3/linux-gnu-c-opt/lib -lcmumps -ldmumps -lsmumps -lzmumps -lmumps_common -lpord -lumfpack -lklu -lcholmod -lbtf -lccolamd -lcolamd -lcamd -lamd -lsuitesparseconfig -lml -lHYPRE -lscalapack -lexoIIv2for -lexodus -llapack -lblas -lparmetis -Wl,-rpath,/usr/lib -L/usr/lib -lnetcdf -ltriangle -lmetis -lchaco -lhwloc -lctetgen -lhdf5_openmpi -lhdf5_openmpi_hl -lX11 -lptesmumps -lptscotch -lptscotcherr -lscotch -lscotcherr -lm -Wl,-rpath,/usr/lib/openmpi/lib -L/usr/lib/openmpi/lib -Wl,-rpath,/usr/lib/gcc/x86_64-linux-gnu/5 -L/usr/lib/gcc/x86_64-linux-gnu/5 -Wl,-rpath,/usr/lib/x86_64-linux-gnu -L/usr/lib/x86_64-linux-gnu -Wl,-rpath,/lib/x86_64-linux-gnu -L/lib/x86_64-linux-gnu -lmpi_usempif08 -lmpi_usempi_ignore_tkr -lmpi_mpifh -lgfortran -lm -lgfortran -lm -lquadmath -lm -lmpi_cxx -lstdc++ -lrt -lm -lz -Wl,-rpath,/usr/lib/openmpi/lib -L/usr/lib/openmpi/lib -Wl,-rpath,/usr/lib/gcc/x86_64-linux-gnu/5 -L/usr/lib/gcc/x86_64-linux-gnu/5 -Wl,-rpath,/usr/lib/x86_64-linux-gnu -L/usr/lib/x86_64-linux-gnu -Wl,-rpath,/lib/x86_64-linux-gnu -L/lib/x86_64-linux-gnu -Wl,-rpath,/usr/lib/x86_64-linux-gnu -L/usr/lib/x86_64-linux-gnu -ldl -Wl,-rpath,/usr/lib/openmpi/lib -lmpi -lgcc_s -lpthread -ldl -lexoIIv2c -lnetcdf -llapack -ludunits2 -lpthread -lm -lstdc++ -L/usr/lib -lpython2.7 -Xlinker -export-dynamic -Wl,-O0 -Wl,-Bsymbolic-functions -L/usr/lib -lz -lpthread -ldl -lutil -L/usr/lib/gcc/x86_64-linux-gnu/5 -L/usr/lib/gcc/x86_64-linux-gnu/5/../../../x86_64-linux-gnu -L/usr/lib/gcc/x86_64-linux-gnu/5/../../../../lib -L/lib/x86_64-linux-gnu -L/lib/../lib -L/usr/lib/x86_64-linux-gnu -L/usr/lib/../lib -L/usr/lib/gcc/x86_64-linux-gnu/5/../../.. -lgfortran -lm -lquadmath -L/usr/lib/gcc/x86_64-linux-gnu/5 -L/usr/lib/gcc/x86_64-linux-gnu/5/../../../x86_64-linux-gnu -L/usr/lib/gcc/x86_64-linux-gnu/5/../../../../lib -L/lib/x86_64-linux-gnu -L/lib/../lib -L/usr/lib/x86_64-linux-gnu -L/usr/lib/../lib -L/usr/lib/gcc/x86_64-linux-gnu/5/../../.. -lgfortran -lm -lquadmath -L./lib   /usr/lib/x86_64-linux-gnu/libz.so /usr/lib/x86_64-linux-gnu/libjsoncpp.so /usr/lib/x86_64-linux-gnu/libexpat.so -lsqlite3 /usr/lib/x86_64-linux-gnu/libvtkRenderingMatplotlib-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkPythonInterpreter-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libpython2.7.so /usr/lib/x86_64-linux-gnu/libfreetype.so /usr/lib/libvtkWrappingTools-6.2.a /usr/lib/x86_64-linux-gnu/libjpeg.so /usr/lib/x86_64-linux-gnu/libpng.so /usr/lib/x86_64-linux-gnu/libtiff.so /usr/lib/x86_64-linux-gnu/libproj.so /usr/lib/x86_64-linux-gnu/libvtkInteractionImage-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkRenderingImage-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkIOParallel-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkIONetCDF-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libnetcdf_c++.so /usr/lib/x86_64-linux-gnu/libnetcdf.so /usr/lib/x86_64-linux-gnu/hdf5/serial/lib/libhdf5.so -lpthread /usr/lib/x86_64-linux-gnu/libsz.so /usr/lib/x86_64-linux-gnu/libdl.so -lm /usr/lib/x86_64-linux-gnu/hdf5/serial/lib/libhdf5_hl.so /usr/lib/x86_64-linux-gnu/libvtkRenderingParallelLIC-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkRenderingLIC-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkRenderingFreeTypeOpenGL-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkIOParallelXML-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libtheoraenc.so /usr/lib/x86_64-linux-gnu/libtheoradec.so /usr/lib/x86_64-linux-gnu/libogg.so /usr/lib/x86_64-linux-gnu/libvtkIOImport-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkIOODBC-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkIOInfovis-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libxml2.so /usr/lib/x86_64-linux-gnu/libvtkFiltersHyperTree-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkFiltersParallelFlowPaths-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkIOVPIC-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkVPIC-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkIOExport-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkRenderingGL2PS-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkRenderingContextOpenGL-6.2.so.6.2.0 /usr/lib/libgl2ps.so /usr/lib/x86_64-linux-gnu/libvtkIOFFMPEG-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkIOMovie-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkFiltersReebGraph-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkRenderingExternal-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkFiltersParallelStatistics-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkFiltersParallelGeometry-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkWrappingJava-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkIOPLY-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkRenderingVolumeOpenGL-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkImagingStatistics-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkTestingGenericBridge-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkIOParallelExodus-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkFiltersSelection-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkIOMPIImage-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkIOEnSight-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkIOGeoJSON-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkFiltersPython-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkFiltersParallelImaging-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkIOParallelNetCDF-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkIOAMR-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkImagingStencil-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkIOMySQL-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkRenderingFreeTypeFontConfig-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkIOGDAL-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkIOVideo-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkLocalExample-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkTestingIOSQL-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkFiltersSMP-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkIOParallelLSDyna-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkFiltersParallelMPI-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkIOXdmf2-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkImagingMath-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkFiltersVerdict-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkFiltersTexture-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkRenderingParallel-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkTestingRendering-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkFiltersProgrammable-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkIOMINC-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkImagingMorphological-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkDomainsChemistry-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkRenderingLOD-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkViewsContext2D-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkInfovisBoostGraphAlgorithms-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkIOPostgreSQL-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkIOMPIParallel-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkParallelMPI4Py-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkViewsGeovis-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkFiltersGeneric-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkFiltersFlowPaths-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libtheoraenc.so /usr/lib/x86_64-linux-gnu/libtheoradec.so /usr/lib/x86_64-linux-gnu/libogg.so /usr/lib/x86_64-linux-gnu/libvtkIOExodus-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkexoIIc-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libnetcdf_c++.so /usr/lib/x86_64-linux-gnu/libnetcdf.so /usr/lib/x86_64-linux-gnu/libvtkWrappingPython27Core-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkFiltersAMR-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkIOLSDyna-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkxdmf2-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/hdf5/serial/lib/libhdf5.so -lpthread /usr/lib/x86_64-linux-gnu/libsz.so /usr/lib/x86_64-linux-gnu/libdl.so -lm /usr/lib/x86_64-linux-gnu/hdf5/serial/lib/libhdf5_hl.so /usr/lib/x86_64-linux-gnu/libxml2.so /usr/lib/x86_64-linux-gnu/libvtkverdict-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkFiltersParallel-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkRenderingOpenGL-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libGLU.so /usr/lib/x86_64-linux-gnu/libSM.so /usr/lib/x86_64-linux-gnu/libICE.so /usr/lib/x86_64-linux-gnu/libX11.so /usr/lib/x86_64-linux-gnu/libXext.so /usr/lib/x86_64-linux-gnu/libXt.so /usr/lib/x86_64-linux-gnu/libvtkIOSQL-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libpython2.7.so /usr/lib/x86_64-linux-gnu/libvtkParallelMPI-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkParallelCore-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkIOLegacy-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkGeovisCore-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkIOXML-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkIOGeometry-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkIOXMLParser-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libproj.so /usr/lib/x86_64-linux-gnu/libvtkViewsInfovis-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkInfovisLayout-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkViewsCore-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkInteractionWidgets-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkFiltersModeling-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkImagingHybrid-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkIOImage-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkIOCore-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkDICOMParser-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkmetaio-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libz.so /usr/lib/x86_64-linux-gnu/libvtkInteractionStyle-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkFiltersHybrid-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkRenderingAnnotation-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkImagingColor-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkRenderingVolume-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkRenderingLabel-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkChartsCore-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkInfovisCore-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkRenderingContext2D-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkRenderingFreeType-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkRenderingCore-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkFiltersGeometry-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkCommonColor-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkFiltersExtraction-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkftgl-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libfreetype.so /usr/lib/x86_64-linux-gnu/libGL.so /usr/lib/x86_64-linux-gnu/libvtkFiltersImaging-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkFiltersStatistics-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkalglib-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkImagingFourier-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkImagingGeneral-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkImagingSources-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkImagingCore-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkFiltersSources-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkFiltersGeneral-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkFiltersCore-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkCommonExecutionModel-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkCommonComputationalGeometry-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkCommonDataModel-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkCommonMisc-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkCommonTransforms-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkCommonMath-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkCommonSystem-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtkCommonCore-6.2.so.6.2.0 /usr/lib/x86_64-linux-gnu/libvtksys-6.2.so.6.2.0 -ldl -Wl,-rpath,/usr/lib/x86_64-linux-gnu/hdf5/serial/lib   -lblas  -L/usr/lib/gcc/x86_64-linux-gnu/5 -L/usr/lib/gcc/x86_64-linux-gnu/5/../../../x86_64-linux-gnu -L/usr/lib/gcc/x86_64-linux-gnu/5/../../../../lib -L/lib/x86_64-linux-gnu -L/lib/../lib -L/usr/lib/x86_64-linux-gnu -L/usr/lib/../lib -L/usr/lib/gcc/x86_64-linux-gnu/5/../../.. -lgfortran -lm -lquadmath 
FLIBS = -L../lib  -L/usr/lib/gcc/x86_64-linux-gnu/5 -L/usr/lib/gcc/x86_64-linux-gnu/5/../../../x86_64-linux-gnu -L/usr/lib/gcc/x86_64-linux-gnu/5/../../../../lib -L/lib/x86_64-linux-gnu -L/lib/../lib -L/usr/lib/x86_64-linux-gnu -L/usr/lib/../lib -L/usr/lib/gcc/x86_64-linux-gnu/5/../../.. -lgfortran -lm -lquadmath

# These objects are needed in each program as they provide the code related to
# diagnostic output and FLabort:
DEBUG_OBJECTS=../debug/Debug.o ../debug/Debug_Parameters.o

VERTICAL_INTEGRATION = ../bin/vertical_integration
VTKDIAGNOSTIC = ../bin/vtkdiagnostic
FLDIAGNOSTICS = ../bin/fldiagnostics
STREAMFUNCTION_2D = ../bin/streamfunction_2d
FLREDECOMP = ../bin/flredecomp
MESHCONV = ../bin/meshconv
TEST_LAPLACIAN= ../bin/test_laplacian
TEST_LAPLACIAN_VECTOR= ../bin/test_laplacian_vector
VISUALISE_ELEMENTS= ../bin/visualise_elements
GMSH2VTU= ../bin/gmsh2vtu
TRIANGLE2VTU= ../bin/triangle2vtu
#VTU2GMSH= ../bin/vtu2gmsh
VTU2TRIANGLE= ../bin/vtu2triangle
PETSC_READNSOLVE = ../bin/petsc_readnsolve
TEST_PRESSURE_SOLVE = ../bin/test_pressure_solve
PROJECT_TO_CONTINUOUS = ../bin/project_to_continuous
UNIFIEDMESH = ../bin/unifiedmesh
LIBFLUIDITY=-l$(FLUIDITY)
LIBFEMTOOLS=-lfemtools
LIBADAPT=-ladaptivity
CHECKMESH=../bin/checkmesh
PROJECT_VTU=../bin/project_vtu
PROBE_VTU=../bin/probe_vtu
SUPERMESH_DIFFERENCE=../bin/supermesh_difference
DIFFERENTIATE_VTU=../bin/differentiate_vtu
VTU_BINS=../bin/vtu_bins
FLADAPT=../bin/fladapt
TIME_AVERAGE_PARALLEL=../bin/time_average_parallel
VTKPROJECTION=../bin/vtk_projection
PERIODISE=../bin/periodise

BINARIES = $(DRAWTIMNEW) $(MAKTIMUNIFORM) $(VTKDIAGNOSTIC)		\
  $(FLDIAGNOSTICS) $(FLREDECOMP) $(PETSC_READNSOLVE)			\
  $(VERTICAL_INTEGRATION) $(EVMERGE) $(FLADAPT) $(CHECKMESH)		\
  $(PROJECT_VTU) $(PROBE_VTU) $(SUPERMESH_DIFFERENCE)			\
  $(DIFFERENTIATE_VTU) $(VTU_BINS) $(GMSH2VTU)	        		\
  $(PROJECT_TO_CONTINUOUS) $(MESHCONV) 		                        \
  $(TEST_PRESSURE_SOLVE) $(UNIFIEDMESH) $(VTKPROJECTION) $(PERIODISE)	\
  $(STREAMFUNCTION_2D)							\
  $(TEST_LAPLACIAN) 

# Work around Intel compiler bug in visualise elements by simply not
# building it.
ifeq (yes,yes)
BINARIES += $(VISUALISE_ELEMENTS)
endif


.SUFFIXES: .f90 .F90 .c .cpp .o .a 

%.o:	%.f90
	$(FC) $(FCFLAGS) -c $<
%.o:	%.F90
	$(FC) $(FCFLAGS) -c $<
%.o:	%.c
	$(CC) $(CFLAGS) -c $<
%.o:	%.cpp
	$(CXX) $(CXXFLAGS) -c $<

default: $(BINARIES) scripts

scripts:
	mkdir -p ../bin
	for i in *.py ; do cp $$i ../bin/`basename $$i .py` ; done
	for i in *.sh ; do cp $$i ../bin/`basename $$i .sh` ; done

install-version-info: version-info
	@mkdir -p ../bin
	@chmod +x $<
	@cp $< ../bin/$<

.PHONY: install-version-info

.PHONY: install_python

install_python:
	python setup.py bdist --format=tar
	tar -x -C /$(DESTDIR) -f dist/*.tar

$(GMSH2VTU): gmsh2vtu.o gmsh2vtu_main.o lib/
	$(LINKER) -o $@ $(filter %.o,$^) -l$(FLUIDITY) $(LIBS)

$(TRIANGLE2VTU): triangle2vtu.o triangle2vtu_main.o lib/
	$(LINKER) -o $@ $(filter %.o,$^) -l$(FLUIDITY) $(LIBS)

#$(VTU2GMSH): vtu2gmsh.o vtu2gmsh_main.o lib/
#	$(LINKER) -o $@ $(filter %.o,$^) -l$(FLUIDITY) $(LIBS)

$(VTU2TRIANGLE): vtu2triangle.o vtu2triangle_main.o lib/
	$(LINKER) -o $@ $(filter %.o,$^) -l$(FLUIDITY) $(LIBS)

$(PROJECT_TO_CONTINUOUS): project_to_continuous.o project_to_continuous_main.o
	$(LINKER) -o $@ $(filter %.o,$^) -l$(FLUIDITY) $(LIBS)

$(TRIANGLE_TEST_MESH): triangle_test_mesh.o
	$(LINKER) -o $(TRIANGLE_TEST_MESH) $^ $(FLIBS) $(LIBFLUIDITY) $(LIBS)

$(TEST_LAPLACIAN): test_laplacian.o
	$(FLLINKER) -o $@ $(filter %.o,$^) -l$(FLUIDITY) $(LIBS)

$(TEST_LAPLACIAN_VECTOR): test_laplacian_vector.o
	$(FLLINKER) -o $@ $(filter %.o,$^) -l$(FLUIDITY) $(LIBS)

$(VISUALISE_ELEMENTS): visualise_elements.o
	$(FLLINKER) $(CXXFLAGS) -o $@ $(filter %.o,$^) -l$(FLUIDITY) $(LIBS)

$(TIME_AVERAGE_PARALLEL): time_average_parallel.o
	$(FLLINKER) -o $@ $(filter %.o,$^) -l$(FLUIDITY) $(LIBS)

$(VERTICAL_INTEGRATION): Vertical_Integration.o Vertical_Integration_main.o lib/
	$(LINKER) $(CXXFLAGS) -o $@ $(filter %.o,$^) -l$(FLUIDITY) $(LIBS)

$(PETSC_READNSOLVE): petsc_readnsolve_main.o petsc_readnsolve.o \
  lib/
	$(LINKER) $(CXXFLAGS) -o $@ $(filter %.o,$^) -l$(FLUIDITY) $(LIBS)

$(TEST_PRESSURE_SOLVE): test_pressure_solve_main.o test_pressure_solve.o \
  lib/
	$(LINKER) $(CXXFLAGS) -o $@ $(filter %.o,$^) -l$(FLUIDITY) $(LIBS)

# we need a symlink to ../lib, as $(LIBS) contains relative references to
# libraries (i.e. ./lib/libadaptivity.a instead of -ladaptivity)
lib/:
	ln -sf ../lib

Flint_volumeroutines.o:Flint_generalroutines.o
Flint_integralroutines.o:Flint_generalroutines.o

$(VTKDIAGNOSTIC): vtkdiagnostic.cpp lib/
	$(LINKER) $(CXXFLAGS) -I../include -o $(VTKDIAGNOSTIC) vtkdiagnostic.cpp $(LIBS)

$(VTKPROJECTION): vtkprojection.cpp lib/
	$(LINKER) $(CXXFLAGS) -I../include -o $(VTKPROJECTION) vtkprojection.cpp -L../lib/ -l$(FLUIDITY) $(LIBS)

$(PERIODISE): periodise.o lib/
	$(FLLINKER) -o $@ $(filter %.o,$^) -l$(FLUIDITY) $(LIBS)

$(FLDIAGNOSTICS): fldiagnostics.o fldiagnostics_main.o lib/
	$(LINKER) -o $@ $(filter %.o,$^) -l$(FLUIDITY) $(LIBS)

$(STREAMFUNCTION_2D): Streamfunction_2D.o Streamfunction_2D_main.o lib/
	$(LINKER) -o $@ $(filter %.o,$^) -l$(FLUIDITY) $(LIBS)

$(FLREDECOMP): Flredecomp.o Flredecomp_main.o lib/
	$(LINKER) -o $@ $(filter %.o,$^) -l$(FLUIDITY) $(LIBS)

$(MESHCONV): Meshconv.o Meshconv_main.o lib/
	$(LINKER) -o $@ $(filter %.o,$^) -l$(FLUIDITY) $(LIBS)

$(CHECKMESH): Checkmesh.o Checkmesh_main.o lib/
	$(LINKER) -o $@ $(filter %.o,$^) -l$(FLUIDITY) $(LIBS)

$(PROJECT_VTU): Project_Vtu.o Project_Vtu_main.o lib/
	$(LINKER) -o $@ $(filter %.o,$^) -l$(FLUIDITY) $(LIBS)

$(PROBE_VTU): Probe_Vtu.o Probe_Vtu_main.o lib/
	$(LINKER) -o $@ $(filter %.o,$^) -l$(FLUIDITY) $(LIBS)

$(SUPERMESH_DIFFERENCE): Supermesh_Difference.o Supermesh_Difference_main.o lib/
	$(LINKER) -o $@ $(filter %.o,$^) -l$(FLUIDITY) $(LIBS)

$(DIFFERENTIATE_VTU): Differentiate_Vtu.o Differentiate_Vtu_main.o lib/
	$(LINKER) -o $@ $(filter %.o,$^) -l$(FLUIDITY) $(LIBS)

$(VTU_BINS): Vtu_Bins.o Vtu_Bins_main.o lib/
	$(LINKER) -o $@ $(filter %.o,$^) -l$(FLUIDITY) $(LIBS)

$(FLADAPT): Fladapt.o Fladapt_main.o lib/
	$(LINKER) -o $@ $(filter %.o,$^) -l$(FLUIDITY) $(LIBS)

$(UNIFIEDMESH): unifiedmesh.o unifiedmesh_main.o lib/
	$(LINKER) -o $@ $(filter %.o,$^) -l$(FLUIDITY) $(LIBS)

clean:
	rm -f *.o *.mod
	rm -rf build dist fluidity.egg-info 
	rm -f lib

distclean:
	rm -f version-info

