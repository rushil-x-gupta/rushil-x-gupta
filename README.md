# Introduction

### Getting Started with AI on Jetson Nano
# Setting up the Nano: Hardware
   * IMPORTANT: use separate monitor, keyboard, mouse for Jetson Nano setup
   * connect USB wifi adapter to Jetson Nano in case of Wifi trouble
1. Download latest version of Jetpack OS (4.6 as of writing) to work computer
2. Flash microSD card with Jetpack OS using Balena Etcher (make sure disk appears in Balena's GUI)
4. Make sure the jumper is attached to the appropriate pins (J48 for 5V DC power supply, microUSB power supply is default)
5. Insert microSD card into Nano and boot it up
6. Check free memory and swap on Nano with command `free -m` (swap should read `4071`)
    * if swap is not 4071, execute the following commands
    * ```
      //Disable ZRAM:
      sudo systemctl disable nvzramconfig

      //Create 4GB swap file
      sudo fallocate -l 4G /mnt/4GB.swap
      sudo chmod 600 /mnt/4GB.swap
      sudo mkswap /mnt/4GB.swap
      
      //Append the following line to /etc/fstab
      sudo su
      echo "/mnt/4GB.swap swap swap defaults 0 0" >> /etc/fstab
      exit
      
      //REBOOT!
      ```
# Downloading Docker container and Headless mode
1. Create a directory in the Nano terminal called `nvdli-data`
* Image Classification
* Image Regression

<!--
**rushil-x-gupta/rushil-x-gupta** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

Here are some ideas to get you started:

- 🔭 I’m currently working on ...
- 🌱 I’m currently learning ...
- 👯 I’m looking to collaborate on ...
- 🤔 I’m looking for help with ...
- 💬 Ask me about ...
- 📫 How to reach me: ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...
-->
