# HDF5 and NeXus tools (process, diagnose, profile)

Short reference for browsing, validating, scripting, and performance work on HDF5 and NeXus files.

---

## View and browse

| Tool | Notes |
|------|--------|
| **HDFView** | Official GUI; tree browser, attributes, simple image plots. |
| **ViTables** | PyQt-based HDF5 viewer (tables-oriented). |
| **Panoply** | NASA tool; strong for gridded data; often works with HDF5. |
| **NeXpy** | NeXus-oriented Python GUI. |
| **Mantid** | NeXus-heavy reduction/analysis (facilities). |
| **silx** | HDF5/NeXus viewing and utilities (ESRF-style stack). |

---

## Command-line inspection (HDF5)

| Tool | Notes |
|------|--------|
| **h5ls** | List groups/datasets; quick layout. |
| **h5dump** | Dump structure, attributes, subset of data. |
| **h5stat** | File-level statistics. |
| **h5repack** | Copy/repack; change chunking, compression, filters. |
| **h5copy** | Subset copy between files. |
| **h5debug** | Low-level HDF5 debugging. |

*Typical package (Debian/Ubuntu):* `hdf5-tools`

---

## NeXus validation and diagnosis

| Tool | Notes |
|------|--------|
| **punx** | NeXus validation against definitions (community tool). |
| **nxvalidate** | Older NeXus validator; still used in some workflows. |
| **nxconvert** / **nxtranslate** | Legacy NeXus utilities; facility-dependent. |
| **nexusformat** (Python) | Read/write NeXus trees; good for scripted checks. |

---

## Python processing and analysis

| Library | Notes |
|---------|--------|
| **h5py** | General HDF5 I/O; most common for custom pipelines. |
| **hdf5plugin** | Optional compression filters (Blosc, etc.) in Python. |
| **pandas** | HDF5 tables via PyTables or export paths. |
| **xarray** | Labeled arrays; pairs with **h5netcdf** / **netCDF4** when conventions fit. |
| **tifffile** | Not HDF5; useful when comparing TIFF vs HDF5 exports. |

---

## Profiling, layout, and performance

| Approach | Notes |
|----------|--------|
| **h5ls -v** / **h5dump -H** | Chunk shape, filters, dimensions, types. |
| **h5repack** experiments | Change chunking/compression and compare read time. |
| **h5perf** / **h5perf_serial** | HDF5 benchmark utilities (if built/installed). |
| **Custom h5py scripts** | Walk tree; sum dataset byte sizes; locate largest datasets. |

---

## Integrity and corruption

| Tool / approach | Notes |
|-----------------|--------|
| **h5py** open read-only | Catches many structural read errors. |
| **h5debug** | Low-level diagnosis when files are suspect. |
| **h5clear** | Where available, for some recoverable states. |

---

## Facility / beamline stacks (often NeXus-centric)

| Tool | Notes |
|------|--------|
| **Mantid** | SNS/ISIS-style workflows; NeXus I/O. |
| **DAWN** | Diamond workflows. |
| **MATLAB / Igor HDF5 plugins** | Site-specific tooling. |

---

## Minimal starter set

1. **HDFView** + **`h5ls` / `h5dump`** — daily browsing and proof of structure.
2. **Python: `h5py`** — scripting and statistics.
3. **NeXus: `punx` or `nexusformat`** — when you need definition-aware checks beyond “has NX_class”.

---

## Related standards and docs

- **NeXus**: [https://www.nexusformat.org/](https://www.nexusformat.org/)
- **HDF5**: [https://www.hdfgroup.org/](https://www.hdfgroup.org/)
