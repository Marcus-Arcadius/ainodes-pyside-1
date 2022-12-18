# aiNodes - Stable Diffusion Desktop

Please join our Discord for further information: https://discord.gg/XDQm9pk5pd

Welcome to our first alpha release, please expect many improvements in a very short amount of time.


```\n
prerequisities to just run the ui and dont use xformers:
A install of miniconda https://docs.conda.io/en/latest/miniconda.html
After thats working you open a anaconda prompt
in the folder of this codes you do then

conda env create -n ainodes -f environment-installer.yaml

once thats finished you can run setup.bat
setup.bat should than do all the rest of the installation except downloading any models, thats your manual part thats left to you alone
Once it is finished it should start the UI and you can start dreaming.


If you want to run xformers and you got a rtx 3xxx youre lucky as setup.bat will just download and install a ready to go xformers for you.
If you got a rtx 2xxx you may have to compile the codes yourself.
For this you would need : A working conda install, MS Visual Studio 2019 with Windows 10 SDK, Cuda 11.6
https://developer.nvidia.com/cuda-11-6-0-download-archive
https://visualstudio.microsoft.com/thank-you-downloading-visual-studio/?sku=community&rel=16&utm_medium=microsoft&utm_campaign=download+from+relnotes&utm_content=vs2019ga+button
https://www.anaconda.com/products/distribution

install/run:
```\n
conda env create -n ainodes -f environment_310.yaml
conda activate ainodes
conda install pytorch torchvision torchaudio pytorch-cuda=11.6 -c pytorch -c nvidia
git clone https://github.com/facebookresearch/xformers
cd xformers
(optionally) pip install ninja
git submodule update --init --recursive
pip install -r requirements-test.txt
pip install -e .```

then running should be as simple as activating the environment with:
pip install xformers-0.0.14.dev0-cp310-cp310-win_amd64.whl <- thats your binary which may have a different naming

from here run setup.bat 


Linux, macOS installers coming up.
