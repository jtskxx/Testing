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

## 🏝️ Summary 🏝️

1. ⚙️ [NVIDIA GPU Requirements](#%EF%B8%8F-nvidia-gpu-requirements)  
2. 🌴 [HiveOS Setup](#%EF%B8%8F-flight-sheet-configuration)  
3. 🪼 [Linux-CLI Setup](#-linux-cli-setup-)
4. <img src="https://media3.giphy.com/media/v1.Y2lkPTc5MGI3NjExaGtnMHhjZzh3dTMwM3psZ2ZxNDFwbjB2b25zdWdvdzg0bW9nMWd2OSZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9cw/PhYTgixTZOrdFNrxHk/giphy.gif" width="18px"> [Windows Setup](#-windows-setup-)  
5. 🔥 [Recommended GPU Overclocks](#recommended-gpu-overclocks)  

<br/>

### **⚙️ NVIDIA GPU Requirements:**
> [!NOTE]
> To update your NVIDIA GPU driver on HiveOS, please run the following command:
```sh
nvidia-driver-update
```
- **NVIDIA 3000 Series:** Driver version **535+** or newer.
- **NVIDIA 4000 Series:** Driver version **550+**.


> [!IMPORTANT]
> Ensure each of your workers has a **unique worker name**; duplicating worker names is not permitted.

<br/>

## ✈️ Flight Sheet Configuration

### Solo Mining <img src="https://media0.giphy.com/media/v1.Y2lkPTc5MGI3NjExZW1ramN2N3lnZXFrajNod2VzcGhmcWM3ZG56YmVhbGx0NDc0ZGFpZCZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9cw/clOgAGJ5iR1RVx5GUl/giphy.gif" width="18px"> https://github.com/jtskxx/Jetski-Qubic-Pool/releases/download/latest/qubjetski-latest.tar.gz
### PPLNS Mining <img src="https://media0.giphy.com/media/v1.Y2lkPTc5MGI3NjExZW1ramN2N3lnZXFrajNod2VzcGhmcWM3ZG56YmVhbGx0NDc0ZGFpZCZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9cw/clOgAGJ5iR1RVx5GUl/giphy.gif" width="18px"> https://github.com/jtskxx/Jetski-Qubic-Pool/releases/download/latest/qubjetski.PPLNS-latest.tar.gz
![image](https://github.com/user-attachments/assets/ca0c3dfa-57d1-4df0-b38f-3f1ecbb0a454)


> [!IMPORTANT]
> **For instance: "%WAL%-%WORKER_NAME%"**
>
> **%WAL%-** will use the Qubic wallet address that you configured in your HiveOS account.
>
> **-%WORKER_NAME%** will automatically use your HiveOS rig name without requiring you to replace it manually.

<br>

##  <img src="https://media.giphy.com/media/W5eoZHPpUx9sapR0eu/giphy.gif" width="30px" alt="Git"/>&nbsp;<b>Extra Config Arguments</b></p>

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

3000 series ```nvtool --setcoreoffset 150 --setclocks 1500 --setmem 5001 --setmemoffset 2000```  
4000 series ```nvtool --setcoreoffset 150 --setclocks 2400 --setmem 7001 --setmemoffset 2000``` 

<br>

## 🧪 Advanced Settings
### Idle Time Feature
> [!NOTE]
> During the Qubic idling phase, you can run another program or miner.
> 
> The example below is for mining on the Xelis pool (Xelski) https://xelskipool.xyz/
> 
> Launch a flight sheet before with the correct miner and ensure its version matches the one in idle config
> 
> More examples are available on the pool Discord

**Extra Config Arguments Example:**
```json
"idleSettings":{"command":"/hive/miners/rigel/1.19.4/rigel","arguments":"-a xelishashv2 -o stratum+tcp://fr.xelskipool.xyz:9191 -u XELWLT -w %WORKER_NAME%"}
```
<br>

|  Setting 		|  Description 	|
|---	|---	|
|  command 	|  The command/program to execute.	|
|  arguments 	|  The arguments that should be passed to the command/program.	|

<br>

# <img src="https://media1.giphy.com/media/v1.Y2lkPTc5MGI3NjExd2tsdHBlcnl4Z21leWc1aHNyejFmbXJkcjZ5YXJoM2RsMzQ2Z2JvdiZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9cw/WFZvB7VIXBgiz3oDXE/giphy.gif" width="30px"> Linux-CLI Setup <img src="https://media1.giphy.com/media/v1.Y2lkPTc5MGI3NjExd2tsdHBlcnl4Z21leWc1aHNyejFmbXJkcjZ5YXJoM2RsMzQ2Z2JvdiZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9cw/WFZvB7VIXBgiz3oDXE/giphy.gif" width="30px">

x
x
x
# <img src="https://media3.giphy.com/media/v1.Y2lkPTc5MGI3NjExaGtnMHhjZzh3dTMwM3psZ2ZxNDFwbjB2b25zdWdvdzg0bW9nMWd2OSZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9cw/PhYTgixTZOrdFNrxHk/giphy.gif" width="30px"> Windows Setup <img src="https://media3.giphy.com/media/v1.Y2lkPTc5MGI3NjExaGtnMHhjZzh3dTMwM3psZ2ZxNDFwbjB2b25zdWdvdzg0bW9nMWd2OSZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9cw/PhYTgixTZOrdFNrxHk/giphy.gif" width="30px">
x
x
x

