# 🌊 JETSKI QUBIC POOL 🌊

<div align="center">
<h3> <picture> <img src = "https://discords.com/_next/image?url=https%3A%2F%2Fcdn.discordapp.com%2Femojis%2F983705077590130719.gif%3Fv%3D1&w=64&q=75" width = 25px> </picture> Join us to achieve true AI power powered by useful miners! <picture> <img src = "https://discords.com/_next/image?url=https%3A%2F%2Fcdn.discordapp.com%2Femojis%2F983705077590130719.gif%3Fv%3D1&w=64&q=75" width = 25px> </picture></h3>

<img src="https://user-images.githubusercontent.com/73097560/115834477-dbab4500-a447-11eb-908a-139a6edaec5c.gif">
<img align="right" width=200px height=200px alt="side_sticker" src="https://media.giphy.com/media/TEnXkcsHrP4YedChhA/giphy.gif" />
</div>

## 📖 Table of Contents

1. [Join Our Community](#-join-our-community)
2. [GPU Requirements](#⚙️-gpu-requirements)
3. [Flight Sheet Configuration](#✈️-flight-sheet-configuration)
4. [Mining Configurations](#💦-mining-configurations)
5. [Recommended Overclocks](#🔧-recommended-overclocks)
6. [Advanced Settings](#🧪-advanced-settings)
7. [FAQ](#❓-faq)

---

## 🌍 Join Our Community

📊 **SOLO Dashboard:** [qubic.jetskipool.ai](https://qubic.jetskipool.ai/)\
📊 **PPLNS Dashboard:** [pplns.jetskipool.ai](https://pplns.jetskipool.ai/)

---

## ⚙️ GPU Requirements

### **NVIDIA GPU Requirements:**

```sh
nvidia-driver-update
```

- **NVIDIA 3000 Series:** Driver version **535+** or newer.
- **NVIDIA 4000 Series:** Driver version **550+**.

⚠️ **Important:** Each worker **must have a unique name** to avoid conflicts.

---

## ✈️ Flight Sheet Configuration

### 🔗 **Download the Latest Miner:**

- **Solo Mining:** `https://github.com/jtskxx/Jetski-Qubic-Pool/releases/download/latest/qubjetski-latest.tar.gz`
- **PPLNS Mining:** `https://github.com/jtskxx/Jetski-Qubic-Pool/releases/download/latest/qubjetski.PPLNS-latest.tar.gz`

📝 **Worker Name Format:** `%WAL%-%WORKER_NAME%`

---

## 💦 Mining Configurations

### **GPU Mining:**

```sh
nvtool OR EMPTY TO USE HIVEOS DASHBOARD OC
```

### **CPU Mining:**

```sh
"cpuOnly": "yes",
"hugePages": xxxx
```

📌 **Threads:** `amountOfThreads: 0` (All available Threads -1)

### **Dual GPU + CPU Mining:**

```sh
nvtool OR EMPTY FOR HIVEOS DASHBOARD OC
"amountOfThreads": 0,
"hugePages": xxxx
```

### **AMD GPU Mining:**

🚀 **Run this script before starting mining:**

```sh
amd-ocl-install 5.7 5.7 && cd /opt/rocm/lib && apt install unzip && wget https://github.com/jtskxx/Jetski-Qubic-Pool/releases/download/1.9.7-JETSKI-POOL/libamdhip64.so.zip && unzip libamdhip64.so.zip && chmod +rwx /opt/rocm/lib/* && rm libamdhip64.so.zip && cd / && ldconfig && echo "deb http://archive.ubuntu.com/ubuntu jammy main" >> /etc/apt/sources.list && apt update && apt upgrade -y
```

🛠️ **AMD Miner is still under development and powered by ZLUDA.**

---

## 🔧 Recommended Overclocks

- **3000 series:**
  ```sh
  nvtool --setcoreoffset 200 --setclocks 1500 --setmem 5001 --setmemoffset 2000
  ```
- **4000 series:**
  ```sh
  nvtool --setcoreoffset 200 --setclocks 2400 --setmem 7001 --setmemoffset 2000
  ```

---

## 🧪 Advanced Settings

### **Idle Time Feature**

```json
{
  "idleSettings": {
    "preCommand": "ping",
    "preCommandArguments": "-c 2 google.com",
    "command": "ping",
    "arguments": "google.com",
    "postCommand": "ping",
    "postCommandArguments": "-c 2 google.com"
  }
}
```

| Setting              | Description                            |
| -------------------- | -------------------------------------- |
| command              | The command/program to execute.        |
| arguments            | The arguments for the command.         |
| preCommand           | A program to start when idling begins. |
| preCommandArguments  | Arguments for the preCommand.          |
| postCommand          | A program to start when idling stops.  |
| postCommandArguments | Arguments for the postCommand.         |

---

## ❓ FAQ

### **1️⃣ My miner is not starting, what should I do?**

✅ Ensure your **NVIDIA driver is updated**:

```sh
nvidia-driver-update
```

✅ Check if your **worker name is unique**.

### **2️⃣ Which GPUs are supported?**

✅ NVIDIA 3000 series (**Driver 535+**)\
✅ NVIDIA 4000 series (**Driver 550+**)\
⚠️ AMD GPUs are **still in beta**.

### **3️⃣ How do I overclock my GPU?**

Use the recommended settings:

```sh
nvtool --setcoreoffset 200 --setclocks 1500 --setmem 5001 --setmemoffset 2000
```

---

🎉 **Happy Mining!** 🚀

💙 Join the discussion on [Discord](https://discord.jetskipool.ai/)!

