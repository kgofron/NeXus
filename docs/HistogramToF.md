# Histogram


* kg1@lap133454:/media/nvme/imgAccumulate/HDF5_NXS_Hist$ h5dump -n His5_1.h5 
```
HDF5 "His5_1.h5" {
FILE_CONTENTS {
 group      /
 dataset    /NDArrayEpicsTSSec
 dataset    /NDArrayEpicsTSnSec
 dataset    /PrvHstNumBins
 dataset    /PrvHstTimeBin0Ms
 dataset    /PrvHstTimeBinStepMs
 group      /entry
 group      /entry/data
 dataset    /entry/data/data
 group      /entry/instrument
 group      /entry/instrument/detector
 dataset    /entry/instrument/detector/data -> /entry/data/data
 dataset    /entry/instrument/detector/frame_number
 dataset    /entry/instrument/detector/timestamp
 dataset    /timestamp
 }
}
```

* kg1@lap133454:/media/nvme/imgAccumulate/HDF5_NXS_Hist$ h5ls -r His5_1.h5 
```
/                        Group
/NDArrayEpicsTSSec       Dataset {1/Inf}
/NDArrayEpicsTSnSec      Dataset {1/Inf}
/PrvHstNumBins           Dataset {1/Inf}
/PrvHstTimeBin0Ms        Dataset {1/Inf}
/PrvHstTimeBinStepMs     Dataset {1/Inf}
/entry                   Group
/entry/data              Group
/entry/data/data         Dataset {16000}
/entry/instrument        Group
/entry/instrument/detector Group
/entry/instrument/detector/data Dataset, same as /entry/data/data
/entry/instrument/detector/frame_number Dataset {1/Inf}
/entry/instrument/detector/timestamp Dataset {1/Inf}
/timestamp               Dataset {1/Inf, 5/Inf}
kg1@lap133454:/media/nvme/imgAccumulate/HDF5_NXS_Hist$ h5dump -n His5_1.h5 
HDF5 "His5_1.h5" {
FILE_CONTENTS {
 group      /
 dataset    /NDArrayEpicsTSSec
 dataset    /NDArrayEpicsTSnSec
 dataset    /PrvHstNumBins
 dataset    /PrvHstTimeBin0Ms
 dataset    /PrvHstTimeBinStepMs
 group      /entry
 group      /entry/data
 dataset    /entry/data/data
 group      /entry/instrument
 group      /entry/instrument/detector
 dataset    /entry/instrument/detector/data -> /entry/data/data
 dataset    /entry/instrument/detector/frame_number
 dataset    /entry/instrument/detector/timestamp
 dataset    /timestamp
 }
}
```

* kg1@lap133454:/media/nvme/imgAccumulate/HDF5_NXS_Hist$ h5dump -d /entry/data/data His5_1.h5 | head

```
HDF5 "His5_1.h5" {
DATASET "/entry/data/data" {
   DATATYPE  H5T_STD_I64LE
   DATASPACE  SIMPLE { ( 16000 ) / ( 16000 ) }
   DATA {
   (0): 980, 998, 998, 996, 977, 972, 990, 985, 1005, 988, 993, 957, 992,
   (13): 985, 1005, 992, 989, 968, 987, 1002, 1000, 972, 995, 957, 997, 987,
   (26): 991, 993, 976, 951, 989, 987, 1008, 989, 1011, 957, 999, 975, 1010,
   (39): 991, 1007, 963, 997, 982, 999, 965, 1011, 948, 1010, 985, 999, 1000,
   (52): 977, 951, 966, 1000, 1001, 972, 1007, 964, 1011, 976, 974, 1006,
```

* kg1@lap133454:/media/nvme/imgAccumulate/HDF5_NXS_Hist$ h5dump -d /PrvHstTimeBin0Ms His5_1.h5

```
HDF5 "His5_1.h5" {
DATASET "/PrvHstTimeBin0Ms" {
   DATATYPE  H5T_IEEE_F64LE
   DATASPACE  SIMPLE { ( 1 ) / ( H5S_UNLIMITED ) }
   DATA {
   (0): 0
   }
   ATTRIBUTE "NDAttrDescription" {
      DATATYPE  H5T_STRING {
         STRSIZE 22;
         STRPAD H5T_STR_NULLTERM;
         CSET H5T_CSET_ASCII;
         CTYPE H5T_C_S1;
      }
      DATASPACE  SCALAR
      DATA {
      (0): "First bin center (ms)"
      }
   }
   ATTRIBUTE "NDAttrName" {
      DATATYPE  H5T_STRING {
         STRSIZE 17;
         STRPAD H5T_STR_NULLTERM;
         CSET H5T_CSET_ASCII;
         CTYPE H5T_C_S1;
      }
      DATASPACE  SCALAR
      DATA {
      (0): "PrvHstTimeBin0Ms"
      }
   }
   ATTRIBUTE "NDAttrSource" {
      DATATYPE  H5T_STRING {
         STRSIZE 7;
         STRPAD H5T_STR_NULLTERM;
         CSET H5T_CSET_ASCII;
         CTYPE H5T_C_S1;
      }
      DATASPACE  SCALAR
      DATA {
      (0): "Driver"
      }
   }
   ATTRIBUTE "NDAttrSourceType" {
      DATATYPE  H5T_STRING {
         STRSIZE 19;
         STRPAD H5T_STR_NULLTERM;
         CSET H5T_CSET_ASCII;
         CTYPE H5T_C_S1;
      }
      DATASPACE  SCALAR
      DATA {
      (0): "NDAttrSourceDriver"
      }
   }
}
}
```

* kg1@lap133454:/media/nvme/imgAccumulate/HDF5_NXS_Hist$ h5dump -d /PrvHstTimeBinStepMs His5_1.h5

```
HDF5 "His5_1.h5" {
DATASET "/PrvHstTimeBinStepMs" {
   DATATYPE  H5T_IEEE_F64LE
   DATASPACE  SIMPLE { ( 1 ) / ( H5S_UNLIMITED ) }
   DATA {
   (0): 0.00099974
   }
   ATTRIBUTE "NDAttrDescription" {
      DATATYPE  H5T_STRING {
         STRSIZE 24;
         STRPAD H5T_STR_NULLTERM;
         CSET H5T_CSET_ASCII;
         CTYPE H5T_C_S1;
      }
      DATASPACE  SCALAR
      DATA {
      (0): "Bin center spacing (ms)"
      }
   }
   ATTRIBUTE "NDAttrName" {
      DATATYPE  H5T_STRING {
         STRSIZE 20;
         STRPAD H5T_STR_NULLTERM;
         CSET H5T_CSET_ASCII;
         CTYPE H5T_C_S1;
      }
      DATASPACE  SCALAR
      DATA {
      (0): "PrvHstTimeBinStepMs"
      }
   }
   ATTRIBUTE "NDAttrSource" {
      DATATYPE  H5T_STRING {
         STRSIZE 7;
         STRPAD H5T_STR_NULLTERM;
         CSET H5T_CSET_ASCII;
         CTYPE H5T_C_S1;
      }
      DATASPACE  SCALAR
      DATA {
      (0): "Driver"
      }
   }
   ATTRIBUTE "NDAttrSourceType" {
      DATATYPE  H5T_STRING {
         STRSIZE 19;
         STRPAD H5T_STR_NULLTERM;
         CSET H5T_CSET_ASCII;
         CTYPE H5T_C_S1;
      }
      DATASPACE  SCALAR
      DATA {
      (0): "NDAttrSourceDriver"
      }
   }
}
}
```

