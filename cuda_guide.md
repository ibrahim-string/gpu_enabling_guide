Windows

Before doing Anything (For Windows only) 
Open NVIDIA control panel and, in 3D settings, select the High performance NVIDIA GPU. 
Even after doing the above step the GPU doesn't work, then follow the next steps: 
1) Check for any driver updates 
2) Verify your power settings. 
3) Try troubleshooting the specific app-setting in control panel. 

To ckeck if gpu is working or not: 

1) Use the DirectX Diagnostic Tool by pressing Windows key + R, typing "dxdiag"
2) Navigate to the "Display" tab to view your GPU details
3) Open task manager go the "Performance tab" and select GPU to see the current status and usage.




Windows (steps) 

Get started with CUDA toolkit for windows: https://developer.nvidia.com/cuda-toolkit
Choose the appropriate configuration and download CUDA tool kit. 

1) Read this blog to learn CUDA python workflow. 
2) NUMBA: Use this parallelism technique to for accelerated performance. 
3) Use Numba, Cupy, Scikit-CUDA, RAPIDS, PyCUDA, Pytorch. Each have their own interoperability layer between CUDA API and python. 



Linux

For Linux(only Ubuntu distro) use the below following steps: 


Before doing anything check whether GPU is actually getting used
use this command `nvidia-smi` or use `nvidia-smi -l 1` for continous refresh interval of 1 second.

if yes: 

No need to further explore (check of temperature of GPU, GPU utilization)

else No: 

1) Check whether GPU is seen by the system or not: sudo lshw -C
2) Download `ubuntu-drivers devices` (`sudo ubuntu-drivers devices`)	
3) Run nvidia-settings and select Performance in PRIME profiles.
4) After doing all these steps restart your machine. 
Even if the above steps doesn't fix the issue: 
Use `sudo nvidia-xconfig` and reboot your system. 
