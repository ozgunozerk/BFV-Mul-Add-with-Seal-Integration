### This is a demo: Keygen and Encryption is done by the SEAL library, Decryption is done with our custom CUDA code.


# How to Run:
1. Add Visual Studio 2017's cl.exe to PATH environment variable (should be done only once for the fresh install of VS 2017)
3. Go into the repository folder in CMD
4. `cmake build -DCMAKE_CUDA_FLAGS="-arch=sm_30" -G"Visual Studio 15 2017 Win64" .` (change this depending on your VS version)
5. Open the newly created solution (.sln) file in VS2017 (should be generated in the repository folder)
6. Change Debug mode to Release mode in VS2017
7. Righ-Click on SEALCuda on the solution explorer tab. Set as StartUp Project
8. Click "Build" on VS, then Run


P.S.: other variants of SEAL integration with our CUDA code (both encryption and decryption done in CUDA, only encryption done in CUDA, etc...) can be coded easily using the BFV_Scheme
