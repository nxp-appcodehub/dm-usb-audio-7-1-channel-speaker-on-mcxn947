# NXP Application Code Hub
[<img src="https://mcuxpresso.nxp.com/static/icon/nxp-logo-color.svg" width="100"/>](https://www.nxp.com)

## How to implement USB audio 7.1 channel speaker on MCXN947
This demo will show you how to implement a USB audio 7.1 channel speaker on MCXN947.

#### Boards: FRDM-MCXN947, AUD-EXP-42448, MCXN FRDM adapter board
#### Categories: Audio
#### Peripherals: SAI, USB
#### Toolchains: MCUXpresso IDE

## Table of Contents
1. [Software](#step1)
2. [Hardware](#step2)
3. [Setup](#step3)
4. [Results](#step4)
5. [FAQs](#step5) 
6. [Support](#step6)
7. [Release Notes](#step7)

## 1. Software<a name="step1"></a>
- FRDM-MCXN947 SDK 2.14
- MCUXpresso IDE V11.9.0 or later.
- MCUXpresso for Visual Studio Code: This example supports MCUXpresso for Visual Studio Code, for more information about how to use Visual Studio Code please refer [here](https://www.nxp.com/design/training/getting-started-with-mcuxpresso-for-visual-studio-code:TIP-GETTING-STARTED-WITH-MCUXPRESSO-FOR-VS-CODE).

## 2. Hardware<a name="step2"></a>
- FRDM-MCXN947 Rev B
- [AUD-EXP-42448 Rev B](https://www.nxp.com/design/design-center/development-boards/i-mx-evaluation-and-development-boards/multichannel-audio-codec-card-for-evks:AUD-EXP-42448)
- MCXN FRDM adapter board Rev A1
- One type-C USB cable
- Any 3.5mm headphones or speakers

## 3. Setup<a name="step3"></a>
This demo is developed based on MCUXpresso IDE 11.9.0 and FRDM-MCXN947 SDK 2.14, so you need to download the MCUXPresso IDE 11.9.0 or higher version and FRDM-MCXN947 SDK 2.14, then install the SDK to MCUXpresso IDE.

### 3.1 Step 1
1. The SAI interface on the FRDM-MCXN947 J1 header is required, the default configuration of J1-3 is for motor control, so the first step is to modify the connection of J1-3, disconnect SJ10 1-2 and short SJ10 2-3.

    ![Alt text](<image/Figure 4.JPG>)

2. Connect the FRDM-MCXN947, MCXN FRDM adapter board, and AUX-EXP-42448 board as shown in the figure below.

    ![](image/boards.JPG)


### 3.2 Step 2
1. Open MCUXpresso IDE 11.9.0, in the Quick Start Panel, choose **Import from Application Code Hub**

    ![](<image/import from ACH 2.png>)


2. Enter the **demo name** in the search bar.

    ![](<image/ACH.JPG>)

3. Click **copy GitHub link**, MCUXpresso IDE will automatically retrive project attributes, then click **Next>**.

    ![](<image/copy github link.png>)

4. Select **main** branch and then click **Next>**, select the MCUXpresso project, click **Finish** button to complete import.

### 3.3 Step 3
1. Use a type-C USB cable to connect J17 of FRDM-MCXN947 and the USB port of the PC.
2. Then click **Build** button to compile the project.

    ![](<image/Build.png>)

3. Click **Debug** button download the program into the MCXN947.
Exit debug mode of the MCUXpresso IDE and reconnect the PC USB port to FRDM-MCXN947 High-speed USB interface J11.

    ![](image/Figure_3.png)

4. Press "RESET" button to run the program, PC will recognize a 7.1 channel audio device.

    ![Alt text](<image/usb audio device.png>)

## 4. Results<a name="step4"></a>

1. Open the Sound Manager, click the **Configure** button, and then on the **Speak Setup** page, click the **Test** button. The PC will play the test audio. You can listen the test audio by connecting any 3.5mm headphone or speak to the four LINE OUTPUT interfaces (J6, J7, J8, J9) on AUX-EXP-42448 board.

    ![Alt text](<image/audio test.png>)


## 5. FAQs<a name="step5"></a>
No FAQs have been identified for this project.

## 6. Support<a name="step6"></a>


#### Project Metadata
<!----- Boards ----->
[![Board badge](https://img.shields.io/badge/Board-FRDM&ndash;MCXN947-blue)](https://github.com/search?q=org%3Anxp-appcodehub+FRDM-MCXN947+in%3Areadme&type=Repositories)

<!----- Categories ----->
[![Category badge](https://img.shields.io/badge/Category-AUDIO-yellowgreen)](https://github.com/search?q=org%3Anxp-appcodehub+audio+in%3Areadme&type=Repositories)

<!----- Peripherals ----->
[![Peripheral badge](https://img.shields.io/badge/Peripheral-SAI-yellow)](https://github.com/search?q=org%3Anxp-appcodehub+sai+in%3Areadme&type=Repositories) [![Peripheral badge](https://img.shields.io/badge/Peripheral-USB-yellow)](https://github.com/search?q=org%3Anxp-appcodehub+usb+in%3Areadme&type=Repositories)

<!----- Toolchains ----->
[![Toolchain badge](https://img.shields.io/badge/Toolchain-MCUXPRESSO%20IDE-orange)](https://github.com/search?q=org%3Anxp-appcodehub+mcux+in%3Areadme&type=Repositories)

Questions regarding the content/correctness of this example can be entered as Issues within this GitHub repository.

>**Warning**: For more general technical questions regarding NXP Microcontrollers and the difference in expected funcionality, enter your questions on the [NXP Community Forum](https://community.nxp.com/)

[![Follow us on Youtube](https://img.shields.io/badge/Youtube-Follow%20us%20on%20Youtube-red.svg)](https://www.youtube.com/@NXP_Semiconductors)
[![Follow us on LinkedIn](https://img.shields.io/badge/LinkedIn-Follow%20us%20on%20LinkedIn-blue.svg)](https://www.linkedin.com/company/nxp-semiconductors)
[![Follow us on Facebook](https://img.shields.io/badge/Facebook-Follow%20us%20on%20Facebook-blue.svg)](https://www.facebook.com/nxpsemi/)
[![Follow us on Twitter](https://img.shields.io/badge/Twitter-Follow%20us%20on%20Twitter-white.svg)](https://twitter.com/NXP)

## 7. Release Notes<a name="step7"></a>
| Version | Description / Update                           | Date                        |
|:-------:|------------------------------------------------|----------------------------:|
| 1.0     | Initial release on Application Code Hub        | January 30<sup>th</sup> 2024 |

