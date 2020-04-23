# Bulk Extractor with Record Carving (bulk_extractor-rec)

**This repository is based on [bulk_extractor](https://github.com/simsong/bulk_extractor), and specialized in developing record carving scanners. Stable scanners in this repository have been committed to official repository. If you need stable version, I recommend to get from official [bulk_extractor](https://github.com/simsong/bulk_extractor).**

Current scanners I have developed: 
* evtx - EVTX file and EVTX chunks (with generated file header)
* ntfsindx - $INDEX_ALLOCATION record (INDX)
* ntfslogfile - $LogFile record (RSTR/RCRD)
* ntfsmft - $MFT record (FILE)
* ntfsusn - $UsnJrnl:$J record (USN_RECORD_V2/V3/V4) 
* utmp - wtmp/btmp record (utmp)

## Ready to build

The following procedure works on Fedora 31 or above.

### Install required package

```
sudo dnf update
sudo dnf groupinstall development-tools
sudo dnf install flex zlib-devel
sudo dnf install libxml2-devel compat-openssl10-devel tre-devel bzip2-devel libtool gcc-c++
sudo dnf install libewf-devel afflib-devel sqlite-devel --skip-broken
sudo dnf install java-1.8.0-openjdk-devel
```

### Git

```
git clone --recursive https://github.com/4n6ist/bulk_extractor-rec.git
cd bulk_extractor-rec
```

## Build

### Linux

```
sh bootstrap.sh
./configure
make
sudo make install
```

### Windows (exe)

```
cd src_win
./CONFIGURE_F31.bash
make
```

## Documentation & Download

Documentation for record carving and binary are available at https://www.kazamiya.net/bulk_extractor-rec/
