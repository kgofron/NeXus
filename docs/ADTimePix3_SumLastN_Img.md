# Sum LastN img

* TPX3-TEST:HDF1:NDArrayAddress=3

```
kg1@lap133454:/media/nvme/imgAccumulate/NeXus_test$ h5ls -r N3.h5
/                        Group
/NDArrayEpicsTSSec       Dataset {1/Inf}
/NDArrayEpicsTSnSec      Dataset {1/Inf}
/entry                   Group
/entry/data              Group
/entry/data/data         Dataset {512, 512}
/entry/instrument        Group
/entry/instrument/detector Group
/entry/instrument/detector/data Dataset, same as /entry/data/data
/entry/instrument/detector/frame_number Dataset {1/Inf}
/entry/instrument/detector/timestamp Dataset {1/Inf}
/timestamp               Dataset {1/Inf, 5/Inf}
kg1@lap133454:/media/nvme/imgAccumulate/NeXus_test$ h5dump N3.h5 | rg "NX_class|signal|default|interpretation"
      ATTRIBUTE "NX_class" {
      ATTRIBUTE "default" {
         ATTRIBUTE "NX_class" {
         ATTRIBUTE "signal" {
            ATTRIBUTE "interpretation" {
         ATTRIBUTE "NX_class" {
            ATTRIBUTE "NX_class" {
kg1@lap133454:/media/nvme/imgAccumulate/NeXus_test$ h5dump -A N3.h5 | rg -A2 'ATTRIBUTE "(NX_class|default|signal|interpretation)"'
      ATTRIBUTE "NX_class" {
         DATATYPE  H5T_STRING {
            STRSIZE 8;
--
      ATTRIBUTE "default" {
         DATATYPE  H5T_STRING {
            STRSIZE 5;
--
         ATTRIBUTE "NX_class" {
            DATATYPE  H5T_STRING {
               STRSIZE 7;
--
         ATTRIBUTE "signal" {
            DATATYPE  H5T_STRING {
               STRSIZE 5;
--
            ATTRIBUTE "interpretation" {
               DATATYPE  H5T_STRING {
                  STRSIZE 6;
--
         ATTRIBUTE "NX_class" {
            DATATYPE  H5T_STRING {
               STRSIZE 13;
--
            ATTRIBUTE "NX_class" {
               DATATYPE  H5T_STRING {
                  STRSIZE 11;
kg1@lap133454:/media/nvme/imgAccumulate/NeXus_test$ h5dump -A N3.h5 | rg -A8 'ATTRIBUTE "(NX_class|default|signal|interpretation)"'
      ATTRIBUTE "NX_class" {
         DATATYPE  H5T_STRING {
            STRSIZE 8;
            STRPAD H5T_STR_NULLTERM;
            CSET H5T_CSET_ASCII;
            CTYPE H5T_C_S1;
         }
         DATASPACE  SCALAR
         DATA {
--
      ATTRIBUTE "default" {
         DATATYPE  H5T_STRING {
            STRSIZE 5;
            STRPAD H5T_STR_NULLTERM;
            CSET H5T_CSET_ASCII;
            CTYPE H5T_C_S1;
         }
         DATASPACE  SCALAR
         DATA {
--
         ATTRIBUTE "NX_class" {
            DATATYPE  H5T_STRING {
               STRSIZE 7;
               STRPAD H5T_STR_NULLTERM;
               CSET H5T_CSET_ASCII;
               CTYPE H5T_C_S1;
            }
            DATASPACE  SCALAR
            DATA {
--
         ATTRIBUTE "signal" {
            DATATYPE  H5T_STRING {
               STRSIZE 5;
               STRPAD H5T_STR_NULLTERM;
               CSET H5T_CSET_ASCII;
               CTYPE H5T_C_S1;
            }
            DATASPACE  SCALAR
            DATA {
--
            ATTRIBUTE "interpretation" {
               DATATYPE  H5T_STRING {
                  STRSIZE 6;
                  STRPAD H5T_STR_NULLTERM;
                  CSET H5T_CSET_ASCII;
                  CTYPE H5T_C_S1;
               }
               DATASPACE  SCALAR
               DATA {
--
         ATTRIBUTE "NX_class" {
            DATATYPE  H5T_STRING {
               STRSIZE 13;
               STRPAD H5T_STR_NULLTERM;
               CSET H5T_CSET_ASCII;
               CTYPE H5T_C_S1;
            }
            DATASPACE  SCALAR
            DATA {
--
            ATTRIBUTE "NX_class" {
               DATATYPE  H5T_STRING {
                  STRSIZE 11;
                  STRPAD H5T_STR_NULLTERM;
                  CSET H5T_CSET_ASCII;
                  CTYPE H5T_C_S1;
               }
               DATASPACE  SCALAR
               DATA {
```
