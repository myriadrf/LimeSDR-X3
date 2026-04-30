PMOD Connectors
###############

Two ten pin 0.1” pitch right angle PMOD connectors (J15, J19) are connected to the FPGA. Pinout description, dedicated FPGA pins and FPGA I/O standard is shown in Table 14 and Table 15.

.. list-table:: Table 14. PMOD #A connection (J15)
   :header-rows: 1
   :stub-columns: 1

   * - Connector pin
     - Schematic signal name
     - FPGA pin
     - I/O standard
     - Comment
   * - 1
     - PMOD_A_PIN1
     - R25
     - 3.3V
     - 
   * - 2
     - PMOD_A_PIN2
     - P23
     - 3.3V
     - 
   * - 3
     - PMOD_A_PIN3
     - P21
     - 3.3V
     - 
   * - 4
     - PMOD_A_PIN4
     - P19
     - 3.3V
     - 
   * - 7
     - PMOD_A_PIN7
     - R20
     - 3.3V
     - 
   * - 8
     - PMOD_A_PIN8
     - R21
     - 3.3V
     - 
   * - 9
     - PMOD_A_PIN9
     - P15
     - 3.3V
     - 
   * - 10
     - PMOD_A_PIN10
     - P16
     - 3.3V
     - 
   * - 5, 11
     - GND
     - 
     - 
     - 
   * - 6, 12
     - VCC
     - 
     - 
     - 3.3V (default) or 5V selectable power rail.

.. list-table:: Table 15. PMOD #B connection (J19)
   :header-rows: 1
   :stub-columns: 1

   * - Connector pin
     - Schematic signal name
     - FPGA pin
     - I/O standard
     - Comment
   * - 1
     - PMOD_B_PIN1
     - L23
     - 3.3V
     - 
   * - 2
     - PMOD_B_PIN2
     - M24
     - 3.3V
     - 
   * - 3
     - PMOD_B_PIN3
     - M22
     - 3.3V
     - 
   * - 4
     - PMOD_B_PIN4
     - N22
     - 3.3V
     - 
   * - 7
     - PMOD_B_PIN7
     - N19
     - 3.3V
     - 
   * - 8
     - PMOD_B_PIN8
     - P24
     - 3.3V
     - 
   * - 9
     - PMOD_B_PIN9
     - P25
     - 3.3V
     - 
   * - 10
     - PMOD_B_PIN10
     - N23
     - 3.3V
     - 
   * - 5, 11
     - GND
     - 
     - 
     - 
   * - 6, 12
     - VCC
     - 
     - 
     - 3.3V (default) or 5V selectable power rail.

Pins 6 and 12 of each PMOD connector provides output voltage of 3.3V (default) or 5V. To provide 5V instead of 3.3V remove R181 and solder R182 resistor for PMOD#A; remove R203 and solder R204 resistor for PMOD#B as shown in Figure 9 and Figure 10.

.. figure:: /images/PCIe_5GRadio_v3.0_PMODA.png
  :width: 400

  Figure 9: PMOD #A connector

.. figure:: /images/PCIe_5GRadio_v3.0_PMODB.png
  :width: 400
  
  Figure 10: PMOD #B connector