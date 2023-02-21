 # Upscaler -  for jarvis conda env to persist between instance shutdowns, the conda env must be created like this:
 # conda create --prefix /home/upscaler python=3.9 ipykernel mamba -y
 # note: this may differ for fluid stack


conda activate /home/upscaler
cd Real-ESRGAN

Add service account key for Firestone 

pip install basicsr
pip install facexlib
pip install gfpgan
pip install -r requirements.txt
python setup.py develop

Launch the server:
uvicorn upscaling_endpoint:app --host 0.0.0.0 --port 6006


 NOTE:
 if error in linux, try install this lib:
 apt-get install libgl1-mesa-glx

