# ComfyUI Ubuntu Install With RTX 5070Ti
## Install comfyui inside a unique folder with it's own python virtual environment.
### Ubuntu 24.04 With Python 3.12
```
git clone https://github.com/comfyanonymous/ComfyUI [add a custom folder name here, without the brackets.]
cd [custom folder name]
python3 -m venv [custom venv name]
source [custom venv name]/bin/activate
pip install --pre torch torchvision torchaudio --index-url https://download.pytorch.org/whl/nightly/cu128
```

If you get a "Torch not compiled with CUDA enabled" error, uninstall torch with:
```
pip uninstall torch
```
Reinstall torch
```
pip install -r requirements

python main.py
```
Alternatively you follow up the previous command with --listen [this will make comfyui available on your hoem network]

or

--lowvram if you have less than 24gb vram

To see a list of modifiers use the following command.
```
python main.py --help
```
