Here is the Program, ComfyUI and Models with the location of where the models need to go
along with the Links where you need to download them from.

Install in this order:

If you have an INTEL CPU you have to DISABLE the IGPU in device manager under
Display Adapters Intel(R) UHD Graphics 770 before installing ANYTHING or it could cause you
alot of HEADACHES and alot of unnecessary time trying to troubleshoot the problem that not
DISABLING IGPU will cause. This is from my personal experience while trying to install
Fooocus, just trying to save you the problems. 
 


Git        https://git-scm.com/download/win
To install Git, you don't need to change anything, just keep clicking next until installed.
 

ComfyUI    https://github.com/Redtash1/ComfyUI-Windows-Intel-GPUs/releases/download/v0.2.1/ComfyUI_Windows_Intel.exe
To extract ComfyUI just double click and pick where you would to extract it.
Remember once you start installing ComfyUI you can't move the folder.

Now download the Models to their correct folders.

JuggernautXL:     https://civitai.com/models/133005?modelVersionId=782002
Click the download button and put it in the folder
ComfyUI\model\checkpoints
 

Flux Encoders:    https://huggingface.co/comfyanonymous/flux_text_encoders/tree/main
Download these 2 files to folder
ComfyUI\models\clip
 

Flux GGUF:        https://huggingface.co/city96/FLUX.1-schnell-gguf/tree/main
Download this file to folder
ComfyUI\models\unet
 

Flux vae:    https://huggingface.co/black-forest-labs/FLUX.1-schnell/tree/main
Download this file to folder
ComfyUI\models\vae
 


How to install:

If you have an INTEL CPU you have to DISABLE the IGPU in device manager under
Display Adapters Intel(R) UHD Graphics 770 before installing ANYTHING or it could cause
you alot of HEADACHES and alot of unnecessary time trying to troubleshoot the problem that
not DISABLING IGPU will cause. This is from my personal experience while trying to install
Fooocus, just trying to save you the problems. 
 

Run in this order:
1. Run 1st Intel Driver Install.bat
This uninstalls all the Nvidia Drivers and installs all the Intel Drivers and Dependencies
from the requirements.txt file.
 


How to Launch ComfyUI:
If you have an INTEL CPU you have to disable the IGPU in device manager under Display Adapters
Intel(R) UHD Graphics 770 or ComfyUI will open but when you try to generate an image, it will fail
because it will try to use CPU's built-in graphics with is called IGPU. Once you have disabled it
keep window open but minimize it to remind you to re-enable it before you shutdown your computer.
 

To Launch with normal VRAM:
Launch ComfyUI Normal VRAM.bat
To Launch in Low VRAM mode:
Launch ComfyUI Low VRAM.bat
To Launch in Very Slow CPU mode:
Launch ComfyUI CPU Only.bat
 

I PRE-INSTALLED
COMFYUI MANAGER
ComfyUI GGUF
pythongosssss/ComfyUI-Custom-Scripts

AFTER YOU HAVE LAUNCHED COMFYUI, DRAG AND DROP Comfy Flux GGUF 4.json FROM COMFYUI FOLDER ONTO OPENED BROWSER PAGE. 
 


YOU WILL GET A POPUP WARNING IN RED THAT UNETLOADERGGUF FAILED TO LOAD.
 

TO  EASILY FIX THIS, OPEN COMFYUI MANAGER.
 

CLICK CUSTOM NODES MANAGER
 


GO TO TOP LEFT CORNER CLICK FILTER AND CHANGE TO INSTALLED, THEN GO DOWN TO COMFYUI-GGUF AND CLICK ON TRY FIX.
 


AND THEN CLICK ON RESTART AND IT WILL RESTART COMFYUI AND YOU WILL BE GOOD TO START USING COMFYUI.
 

IF YOU GET ANY RED NODES, MAKE SURE YOU HAVE ALL GGUF/MODELS DOWNLOADED AND IN THE CORRECT FOLDERS. IF YOU DO,
THEN OPEN COMFYUI MANAGER AND CLICK INSTALL MISSING CUSTOM NODES AND INSTALL THE MISSING NODES, THEN CLICK UPDATE
ALL TO REFRESH ALL NODES THEN CLICK RESTART AND IT WILL RESTART COMFYUI. IF THAT DOESN'T WORK OPEN COMFYUI MANAGER
AND CLICK FETCH UPDATES AND RESTART. IF THAT DOESN'T WORK OPEN COMFYUI MANAGER UPDATE COMFYUI AND RESTART.
IF YOU DO HAVE PROBLEMS GO TO THIS DISCORD CHANNEL
"INTEL INSIDERS COMMUNITY" "@COMFYUI FOR INTEL ARC USING IPEX".       https://discord.gg/intel


RECOMMENDED WAYS TO UPDATE:
CAUTION WHEN UPDATING ComfyUI:
It could break the Intel Drivers by trying to load the NVIDIA Drivers.
In which case you would have to rerun:
Run 1st Intel Driver Install.bat again and that should resolve the problem. 
To update the ComfyUI code: 
Double click update folder, then double click update_comfyui.bat
or you can update ComfyUI in ComfyUI Manager Menu in WebUI. 

To update ComfyUI with the python dependencies, note that you should ONLY run this if you have issues with python embedded dependencies.
Double click update folder, then double click update_comfyui_and_python_dependencies.bat

TO SHARE MODELS BETWEEN COMFYUI AND ANOTHER UI:
In the ComfyUI directory you will find a file: extra_model_paths.yaml.example
Rename this file to: extra_model_paths.yaml and edit it with your favorite text editor.