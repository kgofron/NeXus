# FileNexus1 plugin

### TPX3-TEST:Nexus1:NDArrayAddress=1

* kg1@lap133454:/media/nvme/imgAccumulate$ python3 -c "import h5py; f=h5py.File('Nexus1.h5'); d=f['/entry/data/data']; print(d.dtype, d.shape)"
  * uint16 (512, 512)

### TPX3-TEST:Nexus1:NDArrayAddress=2

* kg1@lap133454:/media/nvme/imgAccumulate$ python3 -c "import h5py; f=h5py.File('Nexus2.h5'); d=f['/entry/data/data']; print(d.dtype, d.shape)"
  * uint64 (512, 512)


```
kg1@lap133454:/media/nvme/imgAccumulate$ h5dump -H /media/nvme/imgAccumulate/Nexus2.h5 | head -40
HDF5 "/media/nvme/imgAccumulate/Nexus2.h5" {
GROUP "/" {
   ATTRIBUTE "HDF5_Version" {
      DATATYPE  H5T_STRING {
         STRSIZE 6;
         STRPAD H5T_STR_NULLTERM;
         CSET H5T_CSET_ASCII;
         CTYPE H5T_C_S1;
      }
      DATASPACE  SCALAR
   }
   ATTRIBUTE "NeXus_version" {
      DATATYPE  H5T_STRING {
         STRSIZE 5;
         STRPAD H5T_STR_NULLTERM;
         CSET H5T_CSET_ASCII;
         CTYPE H5T_C_S1;
      }
      DATASPACE  SCALAR
   }
   ATTRIBUTE "creator" {
      DATATYPE  H5T_STRING {
         STRSIZE 36;
         STRPAD H5T_STR_NULLTERM;
         CSET H5T_CSET_ASCII;
         CTYPE H5T_C_S1;
      }
      DATASPACE  SCALAR
   }
   ATTRIBUTE "file_name" {
      DATATYPE  H5T_STRING {
         STRSIZE 35;
         STRPAD H5T_STR_NULLTERM;
         CSET H5T_CSET_ASCII;
         CTYPE H5T_C_S1;
      }
      DATASPACE  SCALAR
   }
   ATTRIBUTE "file_time" {
      DATATYPE  H5T_STRING {
``` 
