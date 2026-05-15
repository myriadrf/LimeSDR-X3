RF Path
#######

LimeSDR X3 board has three LMS7002 transceivers and various other RF components like matching networks, RF switches, power amplifiers, attenuators etc. The complete RF structure is as shown in Figure 6.


.. figure:: /images/PCIe_5GRadio_3v0_diagrams_r1_RF.png
  :width: 600

  Figure 6: LimeSDR X3 v1.0 RF block diagram

RF transceiver #1 RF path is the simplest. Each TX and RX channel has two frequency-matched channels that can be selected using a 2:1 RF switches. In addition, each TX path has an RF amplifier after band selection. This gives RF transceiver #1 a MIMO system (2x2) with selectable bands in full duplex configuration.

RF transceiver #2 is designed to work in 3.55GHz bands. Each TX and RX channel have fixed frequency matching dedicated for 5G 3.55GHz band. TX paths have PAs with couplers on their outputs. Coupled ports can be fed to RF transceiver #3 RXn_H inputs and can be used for applications like calibrations, DPD etc. Each RX path got LNA. This allows RF transceiver #2 to be configured as a MIMO system (2x2) with selectable bands in full or half duplex configurations.

RF transceiver #3 is dedicated for calibrations. Calibration signals may be fed to RF transceiver #2 RX channels or can receive coupled TX signal from PAs. The RF transceiver #3 also has several TX and RX channels that are routed to the coaxial connectors.
