# JTSF

Setup:
1) Create a micromamba environment 
micromamba create -n env root=x python=y -c conda-forge (I'm using root 6.24 and python 3.9.6)
activate env (https://github.com/NLeSC/root-conda-recipes/issues/29)
3) pip install -r requirements.txt
4)



NOTES FOR ME--------------
THIS WORKS: \\
micromamba activate deepsf \\
export JTSF_CMSSW_SETUP="NONE" \\
source setup.sh \\
law index --verbose \\ 
-----------------------------
PROBLEM with CMSSW maybe make sure to setup CMSSW after installing root and python. If the CMSSW is already setup it might be compiled with different compilers!
SOLUTION:
Notes
if Root issue
try source $ROOTSYS/bin/thisroot.sh

WARNING this removes the existing root and python! and reinstalls python 3.9.18
micromamba install -c conda-forge gfal2 gfal2-util \\
Check your root config python version:
root-config --python-version
try reinstalling root after gfal2:
micromamba install root
