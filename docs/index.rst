.. toctree::
   :maxdepth: 2
   :hidden:

   Introduction <self>
   documentation/index

Introduction
============

PCIe 5GRadio is software defined radio board based on Lime LMS7002M Field Programmable Radio Frequency (FPRF) transceiver and Xilinx Artix-7 FPGA, through which apps can be programmed to support any type of wireless standard, e.g. UMTS, LTE, 5G, LoRa, GPS, WiFi, Zigbee, RFID, Digital Broadcasting, Radar and many more.

.. figure:: documentation/images/PCIe_5GRadio_v3.0_RealTop.png
  :width: 600
  
  Figure 1: PCIe 5GRadio v3.0 Board

This board is a sophisticated version featuring three LMS7002M transceiver chips which allows to implement various 5G network configurations. It supports 5G non-standalone architecture (NSA) as well as standalone architecture (SA) with simultaneous sniffing implementation using single PCIe interface based board.

The main difference of NSA and SA is that NSA delivers the control data of 5G Radio Networks to the 4G Core, while the SA connects the 5G Radio directly to the 5G core network, and the control data does not depend on the 4G network at all. NSA is a 5G service that does not "stand alone" but is built over an existing 4G network. SA, on the other hand, allows completely independent operation of a 5G service without any interaction with an existing 4G core.

As described above, 5G NSA configuration requires 4G core along 5G Radio Network. PCIe 5GRadio allows to implement such configuration using two dedicated LMS7002M transceivers - one for 4G radio while second delivers 5G radio. Third LMS7002M transceiver may be utilized for calibrations, spectrum sniffing or as a RF feedback for various DSP algorithms running on FPGA.

There is a provision for White Rabbit for high accuracy of synchronization between multiple PCIe 5GRadio cards. The high accuracy of synchronization in White Rabbit is achieved by extending the Precision Time Protocol (PTP, IEEE 1588-2008). This extension has been incorporated into the new 2019 revision of IEEE 1588 standard by the P1588 Working Group. White Rabbit provides sub-nanosecond accuracy and picoseconds precision of synchronization for large distributed systems which is perfect for telco applications.

All these features requires considerable data throughput between PCIe 5GRadio and host processor. Second generation four lane PCI Express (Peripheral Component Interconnect Express) bus is used to manage all the data transfers between the board and host system CPU. Four lane Gen2 PCIe bus is rated for 2 GBytes/s data throughput which is sufficient for 5G NSA and sniffing applications working in parallel.