# 🌊JETSKI QUBIC POOL🌊

<div align="center">
<h3> <picture> <img src = "https://discords.com/_next/image?url=https%3A%2F%2Fcdn.discordapp.com%2Femojis%2F983705077590130719.gif%3Fv%3D1&w=64&q=75" width = 25px>  </picture> Join us to achieve true AI power powered by useful miners! <img src = "https://discords.com/_next/image?url=https%3A%2F%2Fcdn.discordapp.com%2Femojis%2F983705077590130719.gif%3Fv%3D1&w=64&q=75" width = 25px
	<!--horizontal divider(gradiant)-->
	
<img src="https://user-images.githubusercontent.com/73097560/115834477-dbab4500-a447-11eb-908a-139a6edaec5c.gif">
	<img align="right" width=200px height=200px alt="side_sticker" src="https://media.giphy.com/media/TEnXkcsHrP4YedChhA/giphy.gif" />
</div>

### <a target="blank"><img align="center" src="https://raw.githubusercontent.com/rahuldkjain/github-profile-readme-generator/master/src/images/icons/Social/discord.svg" height="30" width="40" /></a> Discord Server: https://discord.jetskipool.ai/


### <picture> <img src = "https://github.com/7oSkaaa/7oSkaaa/blob/main/Images/Statistics.gif?raw=true" width = 30px>  </picture> SOLO Dashboard: https://qubic.jetskipool.ai/
### <picture> <img src = "https://github.com/7oSkaaa/7oSkaaa/blob/main/Images/Statistics.gif?raw=true" width = 30px>  </picture> PPLNS Dashboard: https://pplns.jetskipool.ai/



<br/>

1. ⚙️ [NVIDIA GPU Requirements](#nvidia-gpu-requirements)  
2. 🛠️ [HiveOS Setup](#flight-sheet-configuration)  
3. 🖥️ **The Linux CLI Setup** *(Coming Soon)*  
4. 🪟 **Windows Setup** *(Coming Soon)*  
5. 🚀 [Recommended GPU Overclocks](#recommended-gpu-overclocks)  
 
<br/>


### **⚙️NVIDIA GPU Requirements:**
> [!NOTE]
> To update your NVIDIA GPU driver on HiveOS, please run the following command:
```sh
nvidia-driver-update
```
- **NVIDIA 3000 Series:** Driver version **535+** or newer.
- **NVIDIA 4000 Series:** Driver version **550+**.


> [!IMPORTANT]
> Ensure each of your workers has a **unique worker name**; duplicating worker names is not permitted.


## ✈️Flight Sheet Configuration

### Solo Mining➡️ https://github.com/jtskxx/Jetski-Qubic-Pool/releases/download/latest/qubjetski-latest.tar.gz
### PPLNS Mining➡️ https://github.com/jtskxx/Jetski-Qubic-Pool/releases/download/latest/qubjetski.PPLNS-latest.tar.gz
![image](https://github.com/user-attachments/assets/ca0c3dfa-57d1-4df0-b38f-3f1ecbb0a454)


> [!IMPORTANT]
> **For instance: "%WAL%-%WORKER_NAME%"**
>
> **%WAL%-** will use the Qubic wallet address that you configured in your HiveOS account.
>
> **-%WORKER_NAME%** will automatically use your HiveOS rig name without requiring you to replace it manually.

<br>

##  <img src="https://media.giphy.com/media/W5eoZHPpUx9sapR0eu/giphy.gif" width="30px" alt="Git"/>&nbsp;<b>Extra Config Arguments:</b></p>

### ☀️GPU mining:☀️ ###
```
nvtool OR EMPTY TO USE HIVEOS DASHBOARD OC
```

### 🏖️CPU mining:🏖️ ###
> [!NOTE]
> "amountOfThreads":0 = All available Threads -1
>

`Huge Pages: (100 x Numbers of threads)`
```
"cpuOnly":"yes"
"hugePages":xxxx
```
### ⚡GPU+CPU (Dual mining)⚡ ###
```
nvtool OR EMPTY FOR HIVEOS DASHBOARD OC
"amountOfThreads":0
"hugePages":xxxx
```
## 💦Recommended GPU overclocks💦

3000 series ```nvtool --setcoreoffset 200 --setclocks 1500 --setmem 5001 --setmemoffset 2000```  
4000 series ```nvtool --setcoreoffset 200 --setclocks 2400 --setmem 7001 --setmemoffset 2000``` 

<br>

## 🧪 Advanced Settings:
### Idle Time Feature
> [!NOTE]
> During the Qubic idling phase, you can run another program or miner.

**Extra Config Arguments Example:**
```json
"idleSettings":{"preCommand":"ping","preCommandArguments":"-c 2 google.com","command":"ping","arguments":"google.com","postCommand":"ping","postCommandArguments":"-c 2 google.com"}
```
<br>

|  Setting 		|  Description 	|
|---	|---	|
|  command 	|  The command/program to execute.	|
|  arguments 	|  The arguments that should be passed to the command/program.	|
|  preCommand 	|  A command/program to start once the idling period begins.	|
|  preCommandArguments 	|  The arguments that should be passed to the preCommand/program.	|
|  postCommand 	|  A command/program to start once the idling period stops.	|
|  postCommandArguments 	|  The arguments that should be passed to the postCommand/program.	|
