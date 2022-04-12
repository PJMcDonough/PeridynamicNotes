``` 
 1004  module switch PrgEnv-intel PrgEnv-cray
 1005  module load cray-netcdf-hdf5parallel/4.6.3.2
 1006  module load cray-trilinos/12.14.1.0
 1007  module load cray-hdf5-parallel
 1008  export LD_LIBRARY_PATH=$CRAY_LD_LIBRARY_PATH
 
Tue Apr 12 14:10:31 2022: [unset]:_pmi_alps_init:alps_get_placement_info returned with error -1
Tue Apr 12 14:10:31 2022: [unset]:_pmi_init:_pmi_alps_init returned -1
```
[https://docs.nersc.gov/development/libraries/hdf5/#known-issues-on-cori]
