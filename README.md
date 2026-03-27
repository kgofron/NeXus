# NeXus
NeXus HDF format for neutron data

* h5ls -r N3.h5
* h5dump N3.h5 | rg "NX_class|signal|default|interpretation"
* h5dump -A N3.h5 | rg -A2 'ATTRIBUTE "(NX_class|default|signal|interpretation)"'
* h5dump -A N3.h5 | rg -A8 'ATTRIBUTE "(NX_class|default|signal|interpretation)"'

