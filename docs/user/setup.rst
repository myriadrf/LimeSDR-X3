Hardware Setup
##############

Host Interface
**************

LimeSDR X3 should be connected to the host device via PCIe x4 or bigger connector. 

The host must provide a PCIe x4 Gen2 interface.

Power Supply
************

The board is designed to be powered via a 6-pin PCIe connector (12 V), delivering up to 75 W. If necessary, it can be reconfigured to receive power from the mPCIe slot (12 V, up to 25 W).

Cooling
*******

Depending on the application, host system and ambient temperature, additional cooling may be required to ensure reliable operation of the LimeSDR USB board. This may be in the form of airflow through the host system, or a dedicated heatsink fitted to the board.

The board provides mounting holes and connectors for two standard 60 mm, 12 V DC fans. The fans should be installed above the RF front end and the FPGA. For installation, we recommend using M3 screws with 25 mm M3 spacers. The RF front-end fan should be connected to header J16, and the FPGA fan to header J18.

.. note::
   In the event of errors, instability or reduced performance, check the board temperature to ensure that it is within the specified operating range.

RF Connections
**************

.. figure:: /images/LimeSDR-X3_v1.2_rfcon.png
  :width: 600
  
  Figure 8: LimeSDR X3 board top with RF connector positions

.. table:: Table 1. RF Connectors

  +-----------------------+-----------------------------------------------------------+---------------------+
  | **Connector**         | **description**                                           | **frequency range** |
  +=======================+===========================================================+=====================+
  | MCX (J8)              | RF Transceiver #1 channel 1 transmit low frequency range  | 30 MHz - 1.9 GHz    |
  |                       +-----------------------------------------------------------+---------------------+
  |                       | RF Transceiver #1 channel 1 transmit high frequency range | 2 GHz - 2.6 GHz     |
  +-----------------------+-----------------------------------------------------------+---------------------+
  | MCX (J9)              | RF Transceiver #1 channel 2 transmit low frequency range  | 30 MHz - 1.9 GHz    |
  |                       +-----------------------------------------------------------+---------------------+
  |                       | RF Transceiver #1 channel 2 transmit high frequency range | 2 GHz - 2.6 GHz     |
  +-----------------------+-----------------------------------------------------------+---------------------+
  | MCX (J1)              | RF Transceiver #1 channel 1 receive  low frequency range  | 900 MHz (850 MHz)   |
  |                       +-----------------------------------------------------------+---------------------+
  |                       | RF Transceiver #1 channel 1 receive  high frequency range | 2 GHz - 2.6 GHz     |
  +-----------------------+-----------------------------------------------------------+---------------------+
  | MCX (J2)              | RF Transceiver #1 channel 2 receive low frequency range   | 900 MHz (850 MHz)   |
  |                       +-----------------------------------------------------------+---------------------+
  |                       | RF Transceiver #1 channel 2 receive high frequency range  | 2 GHz - 2.6 GHz     |
  +-----------------------+-----------------------------------------------------------+---------------------+
  | MCX (J10)             | RF Transceiver #2 channel 1 transmit / receive (TDD)      | 3.55 GHz ± 50 MHz   |
  +-----------------------+-----------------------------------------------------------+---------------------+
  | MCX (J12)             | RF Transceiver #2 channel 2 transmit / receive (TDD)      | 3.55 GHz ± 50 MHz   |
  +-----------------------+-----------------------------------------------------------+---------------------+
  | MCX (J11)             | RF Transceiver #2 channel 1 receive                       | 3.55 GHz ± 50 MHz   |
  +-----------------------+-----------------------------------------------------------+---------------------+
  | MCX (J13)             | RF Transceiver #2 channel 2 receive                       | 3.55 GHz ± 50 MHz   |
  +-----------------------+-----------------------------------------------------------+---------------------+
  | MCX (J5)              | RF Transceiver #3 channel 2 receive wide frequency range  | 700 MHz - 2.6 GHz   |
  +-----------------------+-----------------------------------------------------------+---------------------+
  | MCX (J7)              | RF Transceiver #3 channel 2 receive high frequency range  | 3.55 GHz ± 50 MHz   |
  +-----------------------+-----------------------------------------------------------+---------------------+
  | MCX (J4)              | RF Transceiver #3 channel 1 receive wide frequency range  | 700 MHz - 2.6 GHz   |
  +-----------------------+-----------------------------------------------------------+---------------------+
  | MCX (J6)              | RF Transceiver #3 channel 1 receive high frequency range  | 3.55 GHz ± 50 MHz   |
  +-----------------------+-----------------------------------------------------------+---------------------+
  | MCX (J3)              | RF Transceiver #3 channel 2 transmit low frequency range  | 30 MHz - 1.9 GHz    |
  +-----------------------+-----------------------------------------------------------+---------------------+
  | SMA (J22), U.FL (J23) | U.FL to SMA adapter                                       | up to 4 GHz         |
  +-----------------------+-----------------------------------------------------------+---------------------+

.. note::
  In versions v1.1 and v1.0 RF conenctors are MMCX / U.FL (not populated).

.. warning::
   Care should be taken when connecting external RF signals to the RX inputs, to ensure that the maximum safe input power of +10 dBm is not exceeded, as this may cause permanent damage to the device.