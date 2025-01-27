# Introducing the DeepRacer Pi: A Budget-Friendly Compute Module Replacement for AWS DeepRacer

The **DeepRacer Pi** is a custom-designed PCB that serves as a cost-effective replacement for the original AWS DeepRacer compute module. With a production and assembly cost of just **$33**, the DeepRacer Pi brings the power of the **Raspberry Pi Compute Module 4 (CM4)** and the upcoming **Compute Module 5 (CM5)** to your DIY racing projects.

<img src="Images/PiRacer.jpg" alt="PiRacer PCB" width="50%">

## What You Need
To get started with the DeepRacer Pi, you’ll need:
1. **Raspberry Pi CM4 Lite**: 
2. **SD Card**: 
3. **PiCamera V2**:

---

The DeepRacer Pi empowers makers and students to build, modify, and innovate with their AWS DeepRacer cars. it is a small enough package to fit into 1/28th scale car significantly reducing the footprint needed for AWS DeepRacer.




## TODO for DeepRacer Pi Development
1. **Move Camera and unneeded headers**
   - remove the extra header not needed for the servo control
   - move the camera next to the headers to face forward

2. **Implement Battery Monitor**  
   - Add circuitry and software support to monitor battery voltage and health.
   - Display battery status in real-time for improved usability.

3. **Fix USB OTG Support**  
   - Modify USB configuration to enable OTG (On-The-Go) functionality.
   - Ensure compatibility with peripherals and reliable data transfer.
4. **Add Tail light LED**
   - Implement multicolor Tail light indicator
5. **Add Fan header**
   - Enable FAN for additional cooling support
6. **Add UART via serial connector headers**
   - to enable additional debugging


## Setting Up the board

1. **Image SD card with  Ubuntu 22.04**
   - use win+shift+x to enable SSH and Wifi during imaging process
   - Edit /boot/firmware/config.txt
     - Add dtparam=i2c_arm=on
     - Add Start_x=1
     - Add dtoverlay=vc4-fkms-v3d
2. Follow these instructions
   - https://github.com/aws-deepracer-community/deepracer-custom-car

Special Thanks for Lars for all the work he did on the Deepracer-custom-car repo to make this a possibility!

<img src="Images/drpi-cm4-firstload.png" alt="PiRacer PCB" width="50%">



