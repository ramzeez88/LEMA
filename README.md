# LEMA AI - Local Efficient Multitasking Assistant v0.0.1
My take on creating an inteligent local voice assistant with some 'superpowers'. I have tested it on Windows OS only. It's a proof of concept i guess. I always wanted to have a real "Jarvis" ;)
Lema can do a few 'things' like open some apps, open web etc. For a full list of commands go to function.py and read the system prompt :)

Reqirements for python 3.11 :  
- Windows 10/11 OS,
- cuda enabled device with cuda 12.1 support, cuda toolkit from https://developer.nvidia.com/cuda-12-1-0-download-archive  and  then install CUDNN from https://developer.nvidia.com/cudnn, my nvidia driver version 546.33
- Visual Studio Build Tools 2022 ('Desktop Development with C++' ticked and installed),
- conda installed and virtual environment created,
- pytorch with cuda installed pip3 install torch torchvision torchaudio --index-url https://download.pytorch.org/whl/cu121 --no-build-isolation,
- llama-cpp-python (min Version: 0.2.75 , whl file can be downloaded from their releases page https://github.com/abetlen/llama-cpp-python/releases),
- pip3 install faster-whisper --no-build-isolation,
- git clone this repo
- git clone OpenVoice from here https://github.com/myshell-ai/OpenVoice/tree/main to LemaAI folder and the checkpoints can be downloaded from https://myshell-public-repo-host.s3.amazonaws.com/openvoice/checkpoints_1226.zip then extracted to checkpoints folder in OpenVoice (not openvoice) folder.
- move 'lema.mp3' to 'OpenVoice/resources' folder.
- move 'open_voice_main.py' to OpenVoice folder.

So far I have used Hermes-2-Pro-Llama-3-Instruct-Merged-DPO-Q8_0.gguf with not bad results. You may ofcourse use any llm you want. Probably the more B's the better ;)


If you are not worried about sensitive data leaving your computer and/or have less than 12GB VRAM, you can use edge_tts module in python to convert text to speech using Microsoft compute. All you have to do is pip install edge_tts asyncio pygame , then rename Lema_voice_edge_tts.py to Lema_voice.py and in folder 'agents' rename _Utils_edge_tts.py to  _Utils.py.

               
This is a Work In Progress ,so there will be bugs and some things missing. I am working on Lema in my spare time. 


Licence not decided yet.

Please support me on ko-fi.com/ramzeez88  :)
