# WITDOM_SC
Contains all code that can be made available related to WITDOM_SC and COSIC implementations

# HOmomorphic encryption SC
1. Installation of the prerequisites
On ubuntu the following steps need to be taken to install the extra libraries needed to run the program
apt-get install gcc
apt-get install libgmp-dev
apt-get install libmpfr-dev
apt-get install git
apt-get install cmake
git clone https://github.com/quarkslab/NFLlib.git
cd NFLlib/
mkdir _build
cd build/
cmake .. -DCMAKE_BUILD_TYPE=Release -DCMAKE_INSTALL_PREFIX=$HOME/nfllib
make
make test
make install
export LD_LIBARY_PATH=/../nfllib/lib/(path naar folder met libnfllib.so file)

2.Getting started
To run the program open the file solution_fraud_detection_witdom and change the necessary parameters in the main part of the program, more specifically the file with inputs, number of covariates and the number of training vectors. When you change the number of covariates and number of training vectors there might be additional parameter changes needed.
Then compile the program using the following command, with the right references to the folders
g++ -std=c++11 -funroll-loops -Ofast -Wall -g -I NFLlib/include solution_fraud_detection_witdom.cpp -o solution_fraud_detection_witdom -L NFLlib/_build -lnfllib -lmpfr -lgmpxx -lgmp
finally run the program with:
./solution_fraud_detection

3.License
The license of the FV-NFllib and the NFLlib is GPLv3.

Author
Charlotte Bonte
