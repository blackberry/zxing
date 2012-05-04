# Blackberry Port of ZXing 2.0 (Zebra Crossing) 
 
Officially sanctioned port of ZXing to the Blackberry/QNX platform.

Please direct all inquiries about ZXing to Eduardo Pelegri-Llopart (epelegrillopart@rim.com).

### Prerequisites

- Blackberry Native SDK (NDK) for Tablet OS

### Build instructions

1. Source the bbndk-env.sh from the NDK installation directory (e.g. ". ./bbndk-env.sh")
2. From the command-line, change to the zxing/cpp/core directory.
3. Run make to produce release and debug shared lib builds of ZXing for ARM and X86.
4. To create static libraries for test purposes, run make in each of the variant directories as required (e.g. if doing a release test on ARM, change to arm/a-le-v7 and run "make").

### Building the tests 

The CppUnit library is required to compile the unit tests. A port is hosted at git@github.com:blackberry/CppUnit.git.  Please clone that repo and follow the same general instructions above except navigating to the root directory of the CppUnit module.  

1. Ensure that the cppunit project is located at the same directory level as the zxing project, as this is what the Makefile expects.
2. From the command-line, change to the zxing/cpp/core/tests directory.
4. Run make to produce release and debug builds of the test binary (zxing-test) for ARM.

### Notes

- Building on Linux from command-line works. Mac and Windows have not been tested.

### TODO

