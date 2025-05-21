
____________________________________________________
# Run Experiments
You need Docker desktop in your local machine 
- Clone this git repository
- in the same root where docker-compose.yml and dockerfile live run
  - `~ docker compose --compatibility up`
    - This will active your docker container and jupyterlab in your terminal 
- To open jupyterlab, choose your browser 
  - copy past this in your browser `http://localhost:8000/lab`
  - jupyterlab passcode `fredy_rojas`

____________________________________________________
# Add python libraries 
Within container JupyterLab terminal 
- pip install "python library" 
- ensure that you are in workspace and then pip freeze
  - `~ pwd`
    /workspace
  - `~ pip freeze | grep -v "feedstock_root" > requirements.txt`


**Note:**
Depending of your GPU and cuda version, you may need to update 
- `Dockerfile` based image: `nvidia/cuda:12.2.2-runtime-ubuntu22.04`
- Pytorch: Current installation
    - `pip3 install torch torchvision torchaudio --index-url https://download.pytorch.org/whl/cu118`
      - `torch==2.7.0+cu118`
      - `torchaudio==2.7.0+cu118`
      - `torchvision==0.22.0+cu118`

____________________________________________________