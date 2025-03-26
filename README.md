# comfyui-install

ubuntu instructions to install comfyui inside a python virtual environment with a custom named folder


git clone https://github.com/comfyanonymous/ComfyUI [add a custom folder name here, without the brackets.]

cd [custom folder name]

python3 -m venv [custom venv name]

source [custom venv name]/bin/activate

pip install --pre torch torchvision torchaudio --index-url https://download.pytorch.org/whl/nightly/cu128

// if you get a "Torch not compiled with CUDA enabled" error, uninstall torch with:

// pip uninstall torch

// install torch again

pip install -r requirements

python main.py

// alternatively you follow up the previous command with --listen [this will make comfyui available on your hoem network]

or

// --lowvram if you have less than 24gb vram

python main.py --help will give you a list of possible modifiers.
