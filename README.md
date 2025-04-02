#
## ComfyUI install on Ubuntu 24.04, Python 3.12, and RTX 5070Ti
### Install comfyui inside a unique folder with it's own python virtual environment.
Instructions to install drivers for your Nvidia Blackwell GPU aka RTX 5090, 5080, 5070, etc can be found here.
https://github.com/tedcor/ubuntu-rtx-5070ti/blob/main/README.md

```
git clone https://github.com/comfyanonymous/ComfyUI [add a custom folder name here, without the brackets.]
cd [custom folder name]
python3 -m venv [custom venv name]
source [custom venv name]/bin/activate
```
##### If you already have pytorch installed you may not have to re-install it and you can skip the pytorch install command below.
##### However if you have any torch related errors, run the install command below followed by --force and it will overwrite current pytorch installation.
```
pipx install --pre torch torchvision torchaudio --index-url https://download.pytorch.org/whl/nightly/cu128
```
To overwrite current pytorch installation
```
pipx install --pre torch torchvision torchaudio --index-url https://download.pytorch.org/whl/nightly/cu128 --force
```

If you get a "Torch not compiled with CUDA enabled" error, uninstall torch with:
```
pip uninstall torch
```
Reinstall torch
```
pip install -r requirements.txt

python main.py
```
Alternatively you follow up the previous command with --listen [this will make comfyui available on your home network]

or

--lowvram if you have less than 24gb vram

To see a list of modifiers use the following command.
```
python main.py --help
```
#
# Custom Nodes
### Below is a list of links to ComfyUI custom nodes. They are easy to install and can save you time.
#
### ComfyUI-Manager

##### Gives you the ablilty to quickly install missing models and nodes.
##### Install to your comfyui/custom_nodes folder.
```
git clone https://github.com/ltdrdata/ComfyUI-Manager comfyui-manager
```
Restart ComfyUI
#
### ComfyUI LoRA Manager
```
git clone https://github.com/willmiao/ComfyUI-Lora-Manager.git comfyui-lora-manager
cd comfyui-lora-manager
pip install -r requirements.txt
```
#### You can launch lora-manager from the ComfyUI menu or by visiting http://localhost:8188/loras
#
