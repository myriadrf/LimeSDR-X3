GNSS Module
###########

GNSS module LYNQ N20B (IC58) can be used not only for positioning applications but for frequency measuring and tuning applications also (e. g. GPS disciplined oscillator - GPSDO). It provides 1PPS time synchronization pulse which is connected to FPGA for further processing. Connection to FPGA is as shown in Table 12.

.. list-table:: Table 12. GNSS module (IC58) connection
   :header-rows: 1
   :stub-columns: 1

   * - Chip pin (IC58)
     - Chip reference (IC58)
     - Schematic signal name
     - FPGA pin
     - I/O standard
   * - 3
     - TIMEPULSE
     - GNSS_TPULSE
     - L20
     - 3.3V
   * - 20
     - UART_TX
     - GNSS_UART_TX
     - L24
     - 3.3V
   * - 21
     - UART_RX
     - GNSS_UART_RX
     - L25
     - 3.3V

External GNSS antenna SMA connector (J21) supports active antennas (3.3V).