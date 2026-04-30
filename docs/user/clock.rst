Reference Clock
###############

The LimeSDR X3 clock system provides multiple high-stability internal clock sources, including a 30.72 MHz VCTCXO (Voltage-Controlled Temperature-Compensated Crystal Oscillator), tunable via an on-board phase detector (IC64) or DAC (IC65), as well as a 100 MHz differential XO dedicated to the FPGA. The board additionally incorporates hardware support for White Rabbit PTP.

The board supports reference clock distribution via dedicated input and output connectors and headers.

.. table:: Table 2. Clock inputs and outputs

  +----------------------+--------------------------+--------------------------------------+
  |     **Function**     | **Connector**            | **Notes**                            |
  +======================+==========================+======================================+
  | External clock input | U.FL (J27 not populated) | 10-52 MHz, 3.3V CMOS                 |
  +----------------------+--------------------------+--------------------------------------+
  | Phase detector input | U.FL (J29)               | 20-300 MHz, 0.8V - 3.3V              |
  +----------------------+--------------------------+--------------------------------------+
  | Clock ouput          | U.FL (J28)               | 30,72 MHz, 3.3 V CMOS                |
  +----------------------+--------------------------+--------------------------------------+
  | PTP clock 2 ouput    | SMA (J25)                | Precision Time Protocol clock output |
  +----------------------+--------------------------+                                      |
  | PTP clock 3 output   | U.FL (J26)               |                                      |
  +----------------------+--------------------------+--------------------------------------+

Synchronization across multiple boards can be achieved via headers J30 and J31 using a daisy-chain topology.

.. table:: Table 3. Synchronization input header (J30)

  +---------+--------------------------------------------+--------------------------------------------------+
  | **Pin** |                **Function**                |                     **Notes**                    |
  +=========+============================================+==================================================+
  |       1 | GND                                        | Ground                                           |
  +---------+--------------------------------------------+--------------------------------------------------+
  |       2 | External clock differential positive input | By default should be used as single ended signal |
  +---------+--------------------------------------------+--------------------------------------------------+
  |       3 | External clock differential negative input | Not populated                                    |
  +---------+--------------------------------------------+--------------------------------------------------+
  |       4 | GND                                        | Ground                                           |
  +---------+--------------------------------------------+--------------------------------------------------+
  |       5 | External PPS input                         | 1 PPS, 3,3 V                                     |
  +---------+--------------------------------------------+--------------------------------------------------+
  |       6 | External Sync input                        | Up to 300 MHz, 3,3 V CMOS                        |
  +---------+--------------------------------------------+--------------------------------------------------+

.. table:: Table 4. Synchronization output header (J31)

  +---------+---------------------------------------------+--------------------------------------------------+
  | **Pin** |                 **Function**                |                     **Notes**                    |
  +=========+=============================================+==================================================+
  |       1 | GND                                         | Ground                                           |
  +---------+---------------------------------------------+--------------------------------------------------+
  |       2 | External clock differential positive output | By default should be used as single ended signal |
  +---------+---------------------------------------------+--------------------------------------------------+
  |       3 | External clock differential negative output | Not populated                                    |
  +---------+---------------------------------------------+--------------------------------------------------+
  |       4 | GND                                         | Ground                                           |
  +---------+---------------------------------------------+--------------------------------------------------+
  |       5 | External PPS output                         | 1 PPS, 3,3 V                                     |
  +---------+---------------------------------------------+--------------------------------------------------+
  |       6 | External Sync output                        | Up to 300 MHz, 3,3 V CMOS                        |
  +---------+---------------------------------------------+--------------------------------------------------+



.. warning::
   When using external clock references, ensure signal levels and frequencies match specifications. 
   
   Improper clock signals may cause unstable operation and potential damage to the device.

