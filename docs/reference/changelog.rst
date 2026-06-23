Changelog
#########

The first production LimeSDR X3 was revision v1.0 and so this changelog starts with changes from that point.

v1.2
****

 * Initial database (created from LimeSDR-X3_1v1(_DB)_DFMr1)
 * Schematic changes:

   * Added shields MECH30, MECH32, MECH31, MECH33, MECH34, MECH35, MECH36, MECH37, MECH38, MECH39, MECH40, MECH41, MECH42, MECH43, MECH44, MECH45 to LMS1, LMS2 and RF switches/LNAs/PAs
   * J1, J2, J3, J4, J5, J6, J7, J8, J9, J10, J11, J12, J13 RF UFL connectors changed to MCX connectors
   * PMOD connectors changed to BHR-12-HUA (with lock)
   * HW_VER changed to 2
   * Updated schematic template
   * Created project variables PROJECT_VERSION and SHEET_TOTAL

 * PCB changes:
  
   * PCB RF part rerouted to fit under shields;
   * Some RF traces on bottom layer routed on L10. Additional requirement for embedded asymetric 50R stripline added to table on mechanical 1
   * PMOD and MCX connector placement updated
   * Project version now comes from variable SHEET_TOTAL on silkscreen and in mechanical 1
   * OCXO thermal case mounting holes increased to 1.5 mm
   * PCIe bracket holes small misalignment fixed

v1.1
****

Schematics of LimeSDR X3 v1.1 board and modifications to the LimeSDR X3 v1.0 board are described in this section. Main changes are as follows:

  * Added ability to disable LMS #1 internal LDO.
  * Changed TX decoupling capacitors.
  * Changed RF TX PAs. 
  * Added ability to choose VVAs DACs Vref.
  * Added common power filters for RF PA power rails.
  * Changed HW_VER to [0 0 0 1].
  * Changed 1,8V power rails voltage regulators.
  * Changed 2,5 V voltage reference.
  * Most of ICs ids changed.

LMS and RF
==========
Added manual config option (LMS1_CORE_LDO_EN) of disabling (disabled by default) LMS #1 (IC1) internal regulators by fitting R6 (fitted by default). See Figure 1 for more details. All other LMSs (LMS#2, LMS#3) on the board already had this option.

.. figure:: /images/PCIe_5GRadio_v3.0_LMS_Changes.png
  :width: 600
  
  Figure 1 LMS #1 core LDO control

Changed RF power amplifiers from TQM8M9079 (VGA) to a combination of 2 QPA4563A PAs and F2258NLGK8 VVA (PA+VVA+PA) due to stock shortages. This was made for both TX channels as shown in Figure 2.

.. figure:: /images/PCIe_5GRadio_v3.0_PA_Changes.png
  :width: 600
  
  Figure 2 RF TX PAs

Changed LMS1_TX1/2 switches decoupling capacitors (C31, C37) from 100 pF to 68pF to match LMS #1 TX PAs (QPA4563A) input at 1950 MHz frequency see Figure 3.

.. figure:: /images/PCIe_5GRadio_v3.0_RFSW_Changes.png
  
  Figure 3 LMS1_TX1/2 switches decoupling capacitors

Power and miscellaneous
=======================

After changing LMS1 TX VGA to discrete (PA+VVA+PA) solution, feedthrough capacitors (C262 and C285) were moved to be able filter each VCC_LMS1_TX1/VCC_LMS1_TX2 power rail.

.. figure:: /images/PCIe_5GRadio_v3.0_PAPWR_Changes.png
  
  Figure 4 RF TX PAs power filtering

Added additional reference voltage selection 2.5 V (default) next to existing 3.3 V and 5.0 V for VVAs (F2258NLGK8) DACs (AD5662) as shown in Figure 5. VVAs attenuation control range depends on supply voltage, but most of attenuation changes in 0.6 V to 2.2 V range as shown in Figure 6, so 2.5 Voltage reference chosen as default and should work for 3.3 V and 5.0V supply voltages.


.. figure:: /images/PCIe_5GRadio_v3.0_VVA1_Changes.png

.. figure:: /images/PCIe_5GRadio_v3.0_VVA2_Changes.png

  Figure 5 VVAs DACs Vref selection


.. figure:: /images/PCIe_5GRadio_v3.0_Vctrl_Changes.png

    Figure 6 (F2258NLGK8) attenuation vs. Vctrl (from datasheet)

Changed 1.8 V power rails voltage switching regulators from LMZ10501 to LMZ20501SILR due to stock shortages.

.. figure:: /images/PCIe_5GRadio_v3.0_V1.8_Changes.png

    Figure 7 new 1.8 V power rails voltage regulators

Changed Voltage reference from MCP1525T to AS431ANTR-G1 due to better pricing and stocking options.

.. figure:: /images/PCIe_5GRadio_v3.0_2.8ref_Changes.png

    Figure 8 new 2.5 V reference

Changed hardware BOM version from [0 0 0 0] to [0 0 0 1] to indicate new version of the board.

.. figure:: /images/PCIe_5GRadio_v3.0_BOMver_Changes.png

    Figure 9 HW_VER

PCB
===

J36 silkscreen fixed (incorrect polarity).

.. figure:: /images/PCIe_5GRadio_v3.0_PCB_Changes.png

    Figure 10 J36 silkscreen fixed

Other minor PCB changes were made related to schematic changes.

LimeSDR X3 v1.1 board 3D views are presented in pictures below.

.. figure:: /images/PCIe_5GRadio_v3.0_PCB_Changes.png

    Figure 11 LimeSDR X3 v1.1 3D view (top)

.. figure:: /images/PCIe_5GRadio_v3.0_PCB_Changes.png

    Figure 12 LimeSDR X3 v1.1 3D view (bottom)

v1.0
****

First production version.