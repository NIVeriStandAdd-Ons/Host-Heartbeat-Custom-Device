## Host Heartbeat Custom Device ##

The **Host Heartbeat Custom Device** is a custom device and VeriStand service that were developed to allow a deployed VeriStand system to recognize when it has lost connection to the host. The target can then alarm off of the disconnection and place itself in a safe state. When added, the custom device provides one channel named "connected?". This channel will have a value of 1 when connected to the host and a value of 0 when not connected.

If you plan on disconnecting then reconnecting with the target, without un-deploying and re-deploying, you'll also need to add the VeriStand service this code contains. When re-connecting (Operate >> Connect) it will check to see if the host daemon is running and, if it isn't, it will start the daemon so it sends heartbeats to the target. 

### LabVIEW Version ###

This code was developed with LabVIEW and VeriStand 2015

### Built Availability ###

No built versions of this code are available. To use the code, download the source and build the code.

### Quality, Limitations ###

This code is fairly simple, and has been tested on both PharLap PXI and Linux cRIOs.

The custom device and service currently only support a single target in the system definition. However, multi-target support is possible with some code modifications.

### Dependencies ###

NI LabVIEW 2015+
NI VeriStand 2015+

### License ###

*This repository and any materials provided by NI therein are provided AS IS. NI DISCLAIMS ANY AND ALL LIABILITIES FOR AND MAKES NO WARRANTIES, EITHER EXPRESS OR IMPLIED, INCLUDING WITHOUT LIMITATION ANY WARRANTIES OF MERCHANTABILITY, FITNESS FOR  PARTICULAR PURPOSE, OR NON-INFRINGEMENT OF INTELLECTUAL PROPERTY. NI shall have no liability for any direct, indirect, incidental, punitive, special, or consequential damages for your use of the repository or any materials contained therein.*