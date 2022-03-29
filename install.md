Patrick’s What to do

Make a map or schematic of how paradigm currently works.
https://en.wikipedia.org/wiki/Linux_kernel#/media/File:Linux_kernel_ubiquity.svg
Looking into the examples directory, consider the flow of what happens.
What actually gets run?
How do we know which functions to edit?
Note that the YAML file causes a runtime selection of models.

Building information

Building Peridigm is not a finished product.
Maybe contribute better documentation.
Change Netcdf to PNetcdf in multiple places?
At some point this may be helpful (https://www.diehlpk.de/blog/builing-peridigm/)
We may have to use an older release of trillinos to avoid having to use a newer version of cmake ughh!

We will install trillinos from source based on peridigm instructions because we want netcdf support. We have to use our own OPEN_MPI_BASE_DIR

Peridigm CMAKE should be run in the root of the git repo with cmake .

What SF did

We start with the supposition that we don’t actually need to build everything ourselves.
No idea why we turned of seacass. We turnned of matio because we don’t like matlab. X11 because why on earth would we want X11!?

Instillation things

penmpi-dev


libpnetcdf-dev


https://github.com/trilinos/trilinos

https://github.com/trilinos/Trilinos/archive/refs/tags/trilinos-release-13-2-0.tar.gz

sudo apt install trilinos-all-dev

libboost-all-dev
libopenmpi-dev
libhdf5-openmpi-dev
libpnetcdf-dev or libnetcdf-dev We don’t know
libnetcdf-dev



# INSTALLATION FOR TRILLINOS 13.0.1

## 13.2.0 Requires new version of cmake!





Grab on CRAY

22) PrgEnv-cray/6.0.10
 23) cray-hdf5-parallel/1.12.1.1
 24) cray-netcdf-hdf5parallel/4.8.1.1
 25) cray-trilinos/12.18.1.1











module switch PrgEnv-intel PrgEnv-cray/6.0.10
module load cray-hdf5-parallel/1.12.1.1
module load cray-netcdf-hdf5parallel/4.8.1.1
module load cray-trilinos/12.18.1.1

rm -f CMakeCache.txt

cmake \
-D CMAKE_INSTALL_PREFIX:PATH="/global/homes/s/sfeister/pkg/peridigm-install" \
-D CMAKE_CXX_FLAGS:STRING="-O2 -Wall -std=c++11 -pedantic -Wno-long-long -ftrapv -Wno-deprecated -fopenmp" \
/global/homes/s/sfeister/pkg/peridigm
