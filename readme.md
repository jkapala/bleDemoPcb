# Overview
This project started with the goal of building a circuit around the STM32 architecture and incorporate various features to evaluate them, which are called out in the Specifications document. A major goal of the project was also to document the project here, making sure to share my progress and use version control. Namely, I wanted to build a board to utilize BLE/WiFi directly, using a PIFA PCB or ceramic chip antenna, instead of using a Wireless module PCB as I have done in the past. As that is the primary goal of the project, other features were secondary but I was able to incorporate a lot of the initial specifications I made and even add some that could lend themselves to a compelling demo of the board. Unfortunately, the STM line of chips does not support WiFi so this could not be integrated into the project so the board will only be BLE-enabled.

## 4/7/2025 Update
The Design Output document is done! I have now edited it and reviewed it so that it is now a complete draft that matches the layout and schematic. The schematic has also been reviewed and edited to fix little things and improve readibility. As well, a few changes were made to the schematic and layout. Namely, a header to access the USB VBUS rail after the current sense resitor has been added, a ground pin has been added to the analog input channel header, and the ESD diodes for the SD card were swapped for ones with lower breakdown/clamping voltage. 

At this stage, I consider all the design files to be in good standing and in agreement with each other. The next step will be to generate a BOM and scrutinize the pinouts of the selected components to the schematics/layout files.

In summary, I believe this commit is a complete draft of both the schematic, layout, and design output.

**Top View**
![3D Render of Top View](./Screenshots/Routing%20done%20-%204.7.2025%20-%20Top%20view.PNG)

**Bottom View**
![3D Render of Top View](./Screenshots/Routing%20done%20-%204.7.2025%20-%20Bottom%20view.PNG)

**Layer View**
![PCB Layout Layer View](./Screenshots/Routing%20done%20-%204.7.2025%20-%20metal%20view.PNG)

## 3/31/2025 Update
Layout of the PCB is finished! I do not expect to change very much now regarding the circuit design or changing the board in any major way. DRC check has run and there are no major issues remaining. Any additional changes should be mainly cosmetic in the PCB and organizational in the schematic files. An additional final check that could necessitate a change is to use the STM32Cube IDE to verify that the pinout for the peripherals is correct, though it was used throughout for this already. The final footprint should focus most interaction to the top of the board. For ease of mounting the referenced LCD character display to the board, a female 2.54mm socket can be attached to the back of the board and the mounting holes in the corners should be aligned so that the screen can be mounted using standoffs/screws.

**Top View**
![3D Render of Top View](./Screenshots/Routing%20done%20-%203.31.2025%20-%20Top%20view.PNG)

**Bottom View**
![3D Render of Top View](./Screenshots/Routing%20done%20-%203.31.2025%20-%20Bottom%20view.PNG)

**Layer View**
![PCB Layout Layer View](./Screenshots/Routing%20done%20-%203.31.2025%20-%20metal%20view.PNG)

The schematic should also specify all part numbers in order to generate a BOM in a future commit. Some passives and minor components remain unspecified because of their generic or non-critical parameters, e.g. specific 0603 LEDs.

The next step is to finalize the Hardware Design Output file by editing the current document to remove extra information, unused part numbers, check individual circuit blocks, part schematics, etc etc. 

## 3/18/2025 Update
Layout is coming along and I am making my way to the STM32 and audio blocks. I decided to get with a ceramic chip antenna instead of the PCB antenna to increase chance of successful RF performance since I don't have RF tools right now. As such, I am using the spatial feedback of the mapped blocks to make final changes in the schematic. For example, I am most likely going to omit the onboard speaker because it really isn't necessary and I can get the version with the plug instead and use that. It looks like I will want to plan to mount the display on the bottomside of the board, otherwise I will cover any exposed pins. This requires moving the connector. Once I get that and the audio block sorted, the rest of the placement should be fairly straightforward.

## 3/7/2025 Update
Layout has started! Finally. I have made a big push to wrap up the schematic layout and do any corresponding research into the various things I wanted to study while building the board, such as RF theory, audio theory, best high-speed layout practices, EMI/EMC topics, etc etc.
The schematic is largely done and should only need adjustment to address bugs or layout improvements. The layout itself is roughly mapped out and currently is sketched to support mounting the chosen LCD screen directly on top of the board, but this require sizeable footprint so I might scrap that idea as I get more blocks placed. I am currently in the stage of doing the rough placing of components relative to the center component (e.g. the STM32, USB PD chip, DC-DC regulators, audio DAC + amp, etc etc). The USB PD block is done and now I am moving on to the DC-DC converters to route power to the downstream circuitry.
