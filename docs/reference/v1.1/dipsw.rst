DIP Switches
############

Four bit DIP switch SW1 is connected to FPGA and may be used to implement additional functionality which requires input control. Each switch line has external pull up resistor. When switch is in position “On”, it pulls the line down to logic ‘0’ level.

.. figure:: /images/LimeSDR-X3_v1.1_DIP_switches.png
  :width: 600
  
  Figure 8: LimeSDR X3 v1.1 four poles slide switch

Switch and FPGA interconnection is as shown in Table 13.

.. list-table:: Table 13. FPGA DIP Switch connections
   :header-rows: 1

   * - Switch pole
     - Schematic signal name
     - FPGA pin (IC29)
     - I/O standard
   * - 1
     - FPGA_SW0
     - K5
     - 2.5V
   * - 2
     - FPGA_SW1
     - L5
     - 2.5V
   * - 3
     - FPGA_SW2
     - G1
     - 2.5V
   * - 4
     - FPGA_SW3
     - G2
     - 2.5V