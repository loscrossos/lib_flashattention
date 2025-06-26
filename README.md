# Flash Attention

This project helps you run the library with support for Nvidia Cuda cards.

- Works in Windows and Linux
- Supports NVidia RTX 50 series:
    - 5090, 5070, 5060
    - 4090, 40xx...
    - 3060, 3090, etc..
- Based on Pytorch 2.7.0
- Works with the latest CUDA Toolkit 12.9



This project will contains a guide to build a fully optimized Library

In the meantime you can have precompiled wheels on the releases page. 

All my libraries are compiled built on each other and work together as a set or independently.

# Install

To use the library first remove the existing entries for this library and paste this into your dependencies file (usually requirements.txt). 
This code snipped is filtered so it works on linux and windows. So you can paste it on both OS.


```
#PYTORCH*********************************************************************

--extra-index-url=https://download.pytorch.org/whl/nightly/cpu ; sys_platform  == 'darwin'
--extra-index-url=https://download.pytorch.org/whl/cu128 ; sys_platform  != 'darwin'
torch==2.7.0
torchaudio

#FLASH ATTENTION****************************
https://github.com/loscrossos/lib_flashattention/releases/download/v2.7.4.post1_crossos00/flash_attn-2.7.4.post1+cu129torch2.7.0-cp312-cp312-linux_x86_64.whl ; sys_platform == 'linux' #egg:v2.7.4.post1
https://github.com/loscrossos/lib_flashattention/releases/download/v2.7.4.post1_crossos00/flash_attn-2.7.4.post1+cu129torch2.7.0-cp312-cp312-win_amd64.whl ; sys_platform == 'win32' #egg:v2.7.4.post1




```
