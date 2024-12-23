## 13.3 TNZ8NS4

TNZ8NS4: 1 x 100G line service processing board

## 13.3.1 Overview

| Board   | Description                            | Board Name (Silkscreen Name)   | Initial Version    |
|---------|----------------------------------------|--------------------------------|--------------------|
| TNZ8NS4 | 1 x 100G line service processing board | NS4                            | V100R009C00 SPC700 |

<!-- image -->

This document describes all boards supported by the device. Whether the boards can be supplied depends on the PCN release result. For details, contact the product manager of the local office.

## Variants

Table 13-13 Available variants of the TNZ8NS4 board

| Variant    | WDM-Side Optical Module                                                          | FEC Encoding   |
|------------|----------------------------------------------------------------------------------|----------------|
| TNZ8NS4    | -                                                                                | -              |
| TNZ8NS4T65 | CFP-100G-(1529.17nm to 1567.1nm)(DWDM,Tunable, high optical power, T65)-SMF      | SDFEC2         |
| TNZ8NS4T5U | 40000 ps/nm-C band-Tunable Wavelength- ePDM-100G QPSK(SDFEC2, ULH+, T5U)-CFP-PIN | SDFEC2         |
| TNZ8NS4T69 | CFP-100G-(1529.17nm to 1567.1nm) (DWDM,Tunable,high optical power, T69)-SMF      | SDFEC2         |

## 13.3.2 Update Description

This section describes the hardware updates in V100R009C00SPC700 and later versions as well as the reasons for the updates. Any product versions that are not listed in the document means that they have no hardware updates.

## Hardware Updates in V100R009C00SPC700

| Hardware Update           | Reason for the Update                                                                                                              |
|---------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| Added the TNZ8NS4 boards. | The NS4 board is a line board that supports hybrid transmission of OTN and packet services with a maximum bandwidth of 100 Gbit/s. |

## 13.3.3 Mappings and Substitution Relationships

## Mapping Relationship

Table 13-14 Mapping relationship of the TNZ8NS4 board

| Board   | Matching Equipment   | Matching System Control Board - Cross- Connect Board   | Version of the Matching System Control and Cross- Connect Board   | Service Capacity     |
|---------|----------------------|--------------------------------------------------------|-------------------------------------------------------------------|----------------------|
| TNZ8NS4 | 1800 V               | TNZ5UXCMS                                              | V100R009C00 SPC700                                                | ● OTN: 100Gbit/s     |
|         |                      | TNZ8XCH                                                |                                                                   | ● Packets: 100Gbit/s |
|         |                      |                                                        |                                                                   | ● OTN:               |
|         |                      |                                                        | V100R009C00                                                       |                      |
|         |                      |                                                        |                                                                   | 100Gbit/s            |
|         |                      |                                                        | SPC700                                                            |                      |

## NO TE

- ● The board inserted on a slave subrack can function only as a pure OTN board.
- ● The board supports only OTN features when it is used together with the TNZ8XCH board.

## RTU

None.

## Substitution

Table 13-15 TNZ8NS4 substitution relationship

| Original Board   | Substitute Board   | Substitute Type       | Restriction                                                                                                                                                                                                                                                                                                                                                                                              |
|------------------|--------------------|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| TNZ8NS 4         | TNZ8UNS4           | Version substitutio n | ● The TNZ8UNS4 board can substitute for the TNZ8NS4 board. The NE software must be upgraded to V100R021C00SPC100 or later. The new board has only the functions of the TNZ8NS4 board. ● The power consumption of the TNZ8UNS4 is greater than that of the TNZ8NS4. If the TNZ8UNS4 is used to replace the TNZ8NS4, ensure that the total power consumption of the chassis does not exceed the threshold. |

## 13.3.4 Front Panel

There are indicators and ports on the front panel of the NS4 board.

## Appearance of the Front Panel

Figure 13-7 Front panel of the NS4 (Color optical modules on the WDM side) boardFigure 13-8 Front panel of the NS4 (Grey optical modules on the WDM side) board

<!-- image -->

Figure 13-7 and Figure 13-8 show the front panel of the NS4 board.

<!-- image -->

## Indicators

- ● Board hardware status indicator (STAT) - red and green
- ● Service status indicator (SRV) - red, green, and orange
- ● WDM-side receive optical power status indicator (IN) - red and green

For details about the indicators, see 31.1 Board Indicators .

Table 13-16 describes the types and functions of the ports on the front panel of the NS4 board.

Table 13-16 Ports on the NS4 board

| Port Silkscre en   | Port Type   | Function                                                                                                               | Required Cable      |
|--------------------|-------------|------------------------------------------------------------------------------------------------------------------------|---------------------|
| IN                 | LC          | Receives single-wavelength signals from the optical demultiplexing unit or the optical add and drop multiplexing unit. | 30.8.4.2 Connectors |
| OUT                | LC          | Transmits single-wavelength signals to the optical multiplexing unit or the optical add and drop multiplexing unit.    | 30.8.4.2 Connectors |
| RX                 | LC          | Receives OTU4 gray light signals.                                                                                      | 30.8.4.2 Connectors |
| TX                 | LC          | Send OTU4 gray light signals.                                                                                          | 30.8.4.2 Connectors |

## Laser Hazard Level

The laser hazard level of the board is HAZARD LEVEL 1, indicating that the maximum output optical power of each optical port is less than 10 dBm (10 mW).

## 13.3.5 Application

The NS4 board is a line board that supports hybrid transmission of OTN and packet services with a maximum bandwidth of 100 Gbit/s. The NS4 board processes and converts the received service signals into one OTU4 signal carried over an ITU-T G.694.1-compliant DWDM wavelength.

## Line Mode

Figure 13-9 illustrates the line mode application of the NS4 board.

## Ports

Figure 13-9 Line mode applicationTable 13-17 Service mapping paths

<!-- image -->

Figure 13-10 illustrates the regeneration mode application of the NS4 board.

<!-- image -->

| Input Signal   | Mapping Path     |
|----------------|------------------|
| Packet         |                  |
| OTN            | ODU0->ODU4->OTU4 |

## NOTE

The total bandwidth of the board does not exceed 100 Gbit/s.

## Regeneration Mode

Figure 13-10 Regeneration mode application

<!-- image -->

## 13.3.6 Functions and Features

## Functions and Features of the TNZ8NS4 Board (OTN Line)

| Function and Feature       | Description                                                                                                                                                                                                                           |
|----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Basic function             | Provides one line port to convert a maximum of 80 channels of ODU0, 40 channels of ODU1, 10 channels of ODU2(e), or 80 channels of ODUflex signals to 1 channel of OTU4. For details about the service mapping path, see Application. |
| Backplane capacity         | The total backplane bandwidth is 100 Gbit/s.                                                                                                                                                                                          |
| WDM specification          | Supports the DWDM specifications.                                                                                                                                                                                                     |
| Tunable wavelength         | Supports tunable wavelength optical modules that provide for 80 wavelengths tunable in the C band with 50 GHz channel spacing.                                                                                                        |
| FEC coding                 | FEC, SDFEC2                                                                                                                                                                                                                           |
| OTN overhead protocol      | Supports the OTN frame format and overhead processing defined by ITU-T G.709.                                                                                                                                                         |
| OTN overhead               | ● WDM-side OTU4 layer: supports SM overhead processing. ● ODUk (k=0, 1, 2, 2e, 3, 4, flex) layer: supports PM and TCM overhead processing. ● ODUk (k=0, 1, 2, 2e, 3, 4, flex) layer: supports non-intrusive monitoring of PM and TCM  |
| Intra-board 1+1            | Supported NOTE Supports intra-board 1+1 protection when working with the OLP board.                                                                                                                                                   |
| protection                 |                                                                                                                                                                                                                                       |
| Tributary SNCP             | Supported NOTE When the cross-connect granularity is ODUflex, the board                                                                                                                                                               |
| Overtemperature protection | does not support tributary SNCP protection. Supported. If the temperature of a board exceeds the upper threshold and services are affected, the board will automatically reset the key chips to prevent a board damage.               |
| Physical clock             | Supported                                                                                                                                                                                                                             |
| IEEE 1588v2                | Not supported                                                                                                                                                                                                                         |

| Function and Feature                   | Description                                                                                                                                                                                                                  |
|----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Outband DCN                            | Supports communication over ESCs. NOTE For details about the DCN types supported by the board, see "Feature Description - Outband DCN - Introduction to DCN - DCN Communication Channel - Comparison Between OSC and ESC".   |
| Optical-layer ASON                     | Supported                                                                                                                                                                                                                    |
| Electrical-layer ASON                  | Supported                                                                                                                                                                                                                    |
| Test frame                             | Not supported                                                                                                                                                                                                                |
| PRBS                                   | Supports the PRBS function on the WDM side.                                                                                                                                                                                  |
| Delay measurement                      | Supported                                                                                                                                                                                                                    |
| Channel loopback                       | Supports channel inloops and outloops. NOTE The total bandwidth of channel inloops on the TNZ8NS4 board must not exceed 40G.                                                                                                 |
| Port loopback                          | Supports WDM-side inloops and outloops.                                                                                                                                                                                      |
| Alarm and performance event monitoring | ● Supports the monitoring of BIP8 bytes (Bursty mode) to help locate line faults. ● Monitors parameters such as the bias current, temperature, and optical power of the laser. ● Monitors OTN alarms and performance events. |

## Functions and Features of the TNZ8NS4 Board (Packet)

| Function and Feature            | Description                                                                                                          |
|---------------------------------|----------------------------------------------------------------------------------------------------------------------|
| Basic function                  | A maximum of 100 Gbit/s packets<->80 x ODU0/80 x ODUflex/40 x ODU1/10 x ODU2/10 x ODU2e/2 x ODU3/1 x ODU4<->1 x OTU4 |
| Backplane bandwidth             | The total backplane bandwidth is 100 Gbit/s.                                                                         |
| Service processing capability   | The maximum service processing capability of the board is 100 Gbit/s.                                                |
| Ethernet data frame format      | IEEE 802.3/Ethernet II/IEEE 802.1q/IEEE 802.1p                                                                       |
| Maximum frame length for a port | 9600 bytes                                                                                                           |
| Service bearing medium          | Port, MPLS-TP, QinQ                                                                                                  |

| Function and Feature                  | Description                                                                                                                                                                                         |
|---------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Native E-Line service type            | ● Point-to-point transparently transmitted E-Line services ● VLAN-based E-Line services ● QinQ-based E-Line services                                                                                |
| Native E-LAN service type             | ● E-LAN service based on the IEEE 802.1d bridge ● E-LAN service based on the IEEE 802.1q bridge                                                                                                     |
| PW-carried E-Line service (VPWS) type | ● Port-based transparently transmitted E-Line services ● VLAN-based E-Line services                                                                                                                 |
| PW-carried E-LAN service (VPLS) type  | ● VPLS services based on Tag-Transparent ● VPLS services based on C-Aware ● VPLS services based on S-Aware                                                                                          |
| MS-PW                                 | Supported                                                                                                                                                                                           |
| HQoS                                  | Supported                                                                                                                                                                                           |
| LPT                                   | Supports point-to-point and point-to-multipoint link-state pass through (LPT) functions. NOTE If the LPT function is configured, the ports on the NS4 board cannot be configured as UNI-side ports. |
| ERPS                                  | Supported                                                                                                                                                                                           |
| LAG                                   | ● Supports load sharing and non-load sharing. ● Supports manual and static aggregation.                                                                                                             |
| MSTP                                  | Not Supported                                                                                                                                                                                       |
| MC-LAG                                | Supported                                                                                                                                                                                           |
| MC-PW APS                             | Supported                                                                                                                                                                                           |
| PW APS                                | Supports 1:1 PW APS.                                                                                                                                                                                |
| PW FPS                                |                                                                                                                                                                                                     |
| Tunnel APS                            | Supports 1:1 PW FPS. ● Supports 1:1 tunnel automatic protection switching (APS).                                                                                                                    |
| MRPS                                  | Supported NOTE MRPS protection can be configured together with PW APS but cannot be configured with tunnel APS.                                                                                     |
| IGMP Snooping                         | Supported                                                                                                                                                                                           |

| Function and Feature   | Description                                                                                                                                                                     |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| LLDP                   | Supported                                                                                                                                                                       |
| Ethernet service OAM   | Supported                                                                                                                                                                       |
| MPLS-TP OAM            | Supported                                                                                                                                                                       |
| RMON                   | Supported                                                                                                                                                                       |
| Port traffic mirroring | Supported                                                                                                                                                                       |
| Physical clock         | Not Supported                                                                                                                                                                   |
| Inband DCN             | Supported                                                                                                                                                                       |
| Jumbo frame            | Supports a jumbo frame containing a maximum of 9600 bytes. NOTE The length of a permitted packet must be no less than 64 bytes and no greater than the specified MFL+ 72 bytes. |

## Functions and Features of the TNZ8NS4 Board (Regeneration)

| Function and Feature       | Description                                                                                                                                                                             |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Basic function             | The board is used in an electrical REG station in the system to implement electrical regeneration of optical signals.                                                                   |
| Regeneration rate          | OTU4                                                                                                                                                                                    |
| WDM specification          | Supports the DWDM specifications.                                                                                                                                                       |
| Tunable wavelength         | Supports tunable wavelength optical modules that provide for 80 wavelengths tunable in the C band with 50 GHz channel spacing.                                                          |
| FEC coding                 | SDFEC2                                                                                                                                                                                  |
| OTN overhead protocol      | Supports the OTN frame format and overhead processing defined by ITU-T G.709.                                                                                                           |
| OTN overhead               | ● WDM-side OTU4 layer: supports SM overhead processing. ● ODU4 layer: supports PM and TCM overhead processing. ● ODU4 layer: supports non-intrusive monitoring of PM and TCM overheads. |
| Intra-board 1+1 protection | Not supported                                                                                                                                                                           |
| ODUk SNCP                  | Not supported                                                                                                                                                                           |

| Function and Feature                   | Description                                                                                                                                                                                                                  |
|----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Tributary SNCP                         | Not supported                                                                                                                                                                                                                |
| Physical clock                         | Not supported                                                                                                                                                                                                                |
| IEEE 1588v2                            | Not supported                                                                                                                                                                                                                |
| Outband DCN                            | Supports communication over ESCs. NOTE For details about the DCN types supported by the board, see "Feature Description - Outband DCN - Introduction to DCN - DCN Communication Channel - Comparison                         |
| Optical-layer ASON                     | Supported                                                                                                                                                                                                                    |
| Test frame                             | Not supported                                                                                                                                                                                                                |
| PRBS                                   | Not supported                                                                                                                                                                                                                |
| Channel loopback                       | Not supported                                                                                                                                                                                                                |
| Alarm and performance event monitoring | ● Supports the monitoring of BIP8 bytes (Bursty mode) to help locate line faults. ● Monitors parameters such as the bias current, temperature, and optical power of the laser. ● Monitors OTN alarms and performance events. |

## 13.3.7 Working Principle and Signal Flow

The NS4 board consists of the signal processing module, WDM-side optical module, control and communication module, and power supply module.

## Functional Modules and Signal Flow

Figure 13-11 shows the functional block diagram of the NS4 board.

Figure 13-11 Functional block diagram of the NS4 board

<!-- image -->

The transmit and receive directions are defined in the signal flow of the NS4 board. The direction from the backplane to the WDM side of the NS4 board is defined as the transmit direction, and the reverse direction is defined as the receive direction.

- ● In the transmit direction:
- -Packet service: The fabric interface circuit processes the data packets from the cross-connect board and maps the packets into the payload of ODUk signals.
- -OTN service:
- i. The ODUk cross-connect module receives the ODUk electrical signals from the cross-connect board through the backplane and transmits the signals to the OTN processing module.
- ii. The OTN processing module produces (by performing operations such as OTN framing and FEC encoding) and transmits one OTU4 electrical signal to the WDM-side optical module.
- iii. After receiving the OTU4 electrical signal, the WDM-side optical module performs E/O conversion and transmits an OTU4 optical signal over an ITU-T G.694.1-compliant DWDM wavelength through the OUT1 port.

- ● In the receive direction:
- -OTN service:
- i. The WDM-side optical module receives one OTU4 optical signal through the IN1 port. Then, the module performs O/E conversion, produces an OTU4 electrical signal, and transmits the signal to the OTN processing module.
- ii. After receiving the OTU4 electrical signal, the OTN processing module performs operations such as FEC decoding, demapping, and demultiplexing, and produces and transmits an ODUk signal to the ODUk cross-connect module.
- iii. The ODUk cross-connect module transmits the ODUk signal to the backplane for grooming.
- -Packet service:

The fabric interface circuit decodes the ODUk signals, performs serial/ parallel conversion, buffers the packets, and transmits them to the crossconnect board through the backplane.

## Module Functions

- ● WDM-side optical module

The optical module consists of a receiver and a transmitter.

- -Receiver: performs O/E conversion of OTU4 signals.
- -Transmitter: performs E/O conversion of OTU4 signals.
- -Reports the performance of client-side optical ports.
- -Reports the working status of WDM-side lasers.
- ● Signal processing module
- -ODUk cross-connect module

Performs cross-connections of ODUk signals through the backplane.

- -OTN processing module
- Frames OTU4 signals, processes the overheads of the OTU4 signals, and performs FEC encoding and decoding.
- ● Switching interface module
- Buffers packets, and manages and schedules queues. It also works with a cross-connect board to form a switching fabric, which performs switching on packets.
- ● Control and Communication Module
- -Controls all operations performed on the board.
- -Collects information about alarms, performance events, working status, and voltage monitoring from each module of the board.
- -Communicates with the system control and communication board.
- ● Power Supply Module

Converts the DC power supplied by the backplane into the power required by each module on the board.

## 13.3.8 Valid Slots

This topic describes the valid slots for the board.

Table 13-18 Valid slots

| Device           |   Num ber of Occu pied Slots | Physical Slot      | Logical Slot   |
|------------------|------------------------------|--------------------|----------------|
| OptiX OSN 1800 V |                            2 | (Slot 2, Slot 3)   | Slot 2         |
| OptiX OSN 1800 V |                            2 | (Slot 4, Slot 5)   | Slot 4         |
| OptiX OSN 1800 V |                            2 | (Slot 9, Slot 10)  | Slot 9         |
| OptiX OSN 1800 V |                            2 | (Slot 11, Slot 12) | Slot 11        |

## NO TE

- ● When an NS4 board is installed in slots 2 and 3 or slots 9 and 10, a maximum of 80 virtual ports are supported in the case of packet services. When an NS4 is installed in slots 4 and 5 or slots 11 and 12, a maximum of 70 virtual ports are supported in the case of packet services.
- ● When the NS4 board functions as a regeneration board, two NS4 boards must be configured and installed in slots 2 and 3 & slots 9 and 10 or slots 4 and 5 & slots 11 and 12.

## Restrictions on Board Insertion

When the board is installed in the OSN 1800 V chassis and works with TNZ5UXCMS, the restricted slots are classified into the following three groups, as shown in Figure 13-12 .

- ● Slots 2, 3, 9, and 10
- ● Slots 4, 5, 11, and 12
- ● Slots 6, 7, 13, and 14

Figure 13-12 Restricted slot groups

<!-- image -->

The use of the following boards in the preceding slot groups is restricted:

- ● Restricted dual-slot boards: TNZ8NS4/TNZ5UNS4/TNZ8UNS4/TNZ5EC1/ TNZ5TSC
- ● Restricted single-slot boards: TNZ5UNQ2/TNZ8UNQ2/TNZ8UTX2/TNZ6UNQ1/ TNZ8NQ2/TNZ8EX4
- ● Special board: TNF1EGS4D

The restrictions are as follows:

- ● When a restricted dual-slot board is installed in the left slot, only one restricted single-slot board can be installed in the right slot of the corresponding slot group.
- For example, when a restricted dual-slot board is installed in slots 2 and 3, only one restricted single-slot board can be installed in either slot 9 or 10.
- ● In each group of slots, the TNF1EGS4D board cannot be installed together with a restricted dual-slot board or restricted single-slot board.

NO TE

The TNZ8NS4/TNZ5UNS4/TNZ8UNS4 board cannot be installed in slot 6, 7, 13, or 14.

## 13.3.9 NS4 Parameters

This topic lists the board parameters that can be set or queried on the NMS.

## Working mode

Table 13-19 Working mode

| Field              | Value                            | Description                                                                                                                                                       |
|--------------------|----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Board Working Mode | Line mode, Electrical relay mode | Specifies the mode that the board supports. Line Mode : The board functions as a line board. Electrical Relay Mode : The board functions as a regeneration board. |

## Parameters for WDM Ports

Table 13-20 Parameters for WDM ports

| Field                      | Value   | Description                                |
|----------------------------|---------|--------------------------------------------|
| Optical Interface/ Channel | -       | Displays the position of the optical port. |
| Optical Interface Name     | -       | Sets the optical port name.                |

| Field                      | Value                                                                     | Description                                                                                                                                                                                                                                                                                                                                                                                                                   |
|----------------------------|---------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Channel Use Status         | Used, Unused Default: Used                                                | Sets the occupancy status of the current channel of a board. When this parameter is set to Unused  for a port, service alarms reported for this port will be masked. This parameter is set to  Used  by default. Set this parameter to                                                                                                                                                                                        |
| Optical Interface Loopback | Non-Loopback, Inloop, Outloop Default: Non- Loopback                      | Specifies the loopback mode for the optical port on a board.                                                                                                                                                                                                                                                                                                                                                                  |
| Channel Loopback           | Non-Loopback, Inloop, Outloop Default: Non- Loopback                      | Sets the channel loopback mode.                                                                                                                                                                                                                                                                                                                                                                                               |
| Laser Status               | Off, On Default: On                                                       | Sets the laser status of a board.                                                                                                                                                                                                                                                                                                                                                                                             |
| FEC Working State          | Enabled, Disabled Default: Enabled                                        | Determines whether to enable or disable the forward error correction (FEC) function for the optical port. For a colored optical module, the FEC function is enabled on the WDM side by default and cannot be disabled. For a gray optical module, disabling the FEC function on the WDM side will cause services to become abnormal, and disabling the FEC function on the clients ide will affect the transmission distance. |
| FEC Mode                   | FEC, SDFEC2 Default: ● Colored optical module: SDFEC2 ● Colorless optical | Sets the FEC mode of the current optical port. The setting of  FEC Mode  for two interconnected boards must be the same.                                                                                                                                                                                                                                                                                                      |

| Field                                                       | Value                                                      | Description                                                                                                                                                                                                                                                                                                      |
|-------------------------------------------------------------|------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| AFEC Grade                                                  | 1, 2, 3 Default: 3                                         | A larger value of this parameter means a stronger error correction capability and a longer signal transmission delay.                                                                                                                                                                                            |
| Band Type/ Wavelength No./ Wavelength (nm)/ Frequency (THz) | -                                                          | Sets the operating wavelength at the WDM-side optical port of a board.                                                                                                                                                                                                                                           |
| Band Type                                                   | -                                                          | Sets the band type.                                                                                                                                                                                                                                                                                              |
| Tunable Wavelength Range                                    | -                                                          | Sets the tunable wavelength range at the WDM-side optical port of a board.                                                                                                                                                                                                                                       |
| Planned Wavelength No./ Wavelength (nm)/ Frequency (THz)    | C: 1/1529.16/196.050 to 80/1560.61/192.100 Default: /      | Sets the wavelength number, wavelength and frequency of the current optical port on the WDM side of a board.                                                                                                                                                                                                     |
| Planned Band Type                                           | C, Follow, / Default: /                                    | Sets the band type of the current working wavelength.                                                                                                                                                                                                                                                            |
| Receive Wavelength                                          | C: 1/1529.16/196.050 to 80/1560.61/192.100 Default: Follow | Specifies the receive wavelength for the board. Observe the following requirements when setting this parameter: ● When the receive wavelength is the same as the transmit wavelength of the board, use the default value so that the receive wavelength automatically keeps the same as the transmit wavelength. |

| Field                                  |                                                                                           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|----------------------------------------|-------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| OTN Overhead Transparently Transmitted | Value Disabled, GCC1+GCC2 Enabled, Only GCC1 Enabled, Only GCC2 Enabled Default: Disabled | Description Determines whether to process GCC1 and GCC2 in OTN overheads. ● When the parameter is set to Disabled , the system will process the GCC1 and GCC2 bytes in the OTN overhead. ● When the parameter is set to GCC1+GCC2 Enabled , the system will not process the GCC1 or GCC2 byte in the OTN overhead. ● When the parameter is set to Only GCC1 Enabled , the system will not process the GCC1 byte but only the GCC2 byte in the OTN overhead. ● When the parameter is set to Only GCC2 Enabled , the system will not process the GCC2 byte but only the GCC1 byte in the OTN overhead. |
| Enable Line Rate                       | -                                                                                         | This parameter is unavailable for the board.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| Line Rate                              | -                                                                                         | This parameter is unavailable for the board.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| PRBS Test Status                       | Enabled, Disabled Default: Disabled                                                       | Sets the pseudo-random binary sequence (PRBS) test status of a board. The PRBS test belongs to the fault diagnosis function and affects channel services. After the PRBS test is started, the services on the corresponding port are interrupted. Different boards support different optical port channels. After the command for enabling the PRBS test is issued, an error is returned                                                                                                                                                                                                             |

| Field                   | Value                                                | Description                                                                                                                                                                                                                                  |
|-------------------------|------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| NULL Mapping Status     | Enabled, Disabled Default: Disabled                  | Determines whether to enable the special frame test before deployment. When this parameter is set to  Enabled , the board sends the test frame where the payload consists of only 0. This parameter is used in the deployment commissioning. |
| ODUflex Tolerance (ppm) | 0 to 100 Default: ● 3GSDI/ 3GSDIRBR: 10 ● CPRI4/6: 1 | Specifies the tolerance of deviation between the actual client-side service rate and the specified rate when the client-side service type is ODUflex.                                                                                        |

## Parameters for Ethernet Ports

Table 13-21 Basic attributes

| Field        | Value                                        | Description                                                                                                                       |
|--------------|----------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| Port         | -                                            | Displays the virtual Ethernet port, for example, 40001(V\_ETH-1).                                                                  |
| Name         | -                                            | Specifies the self-defined port name.                                                                                             |
| Port Enabled | -                                            | This parameter is unavailable for the board.                                                                                      |
| Port Mode    | Layer 2, Layer 3, Layer Mix Default: Layer 2 | Specifies the working mode of the Ethernet port. ● Layer 2 : The port can carry port- based or QinQ-link-based Ethernet services. |

| Field                       | Value                              | Description                                                                                                                                                                  |
|-----------------------------|------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encapsulation Type          | 802.1Q, QinQ, Null Default: 802.1Q | Selects the means of processing the accessed packets. ● This parameter is set to  Null  when the port needs to transparently transmit packets.                               |
| Working Mode                | -                                  | This parameter is unavailable for the board.                                                                                                                                 |
| Max Frame Length (bytes)    | -                                  | Displays the maximum frame length, which is always 9600 bytes. This parameter is not configurable.                                                                           |
| Logical Port Attribute      | -                                  | This parameter is unavailable for the board.                                                                                                                                 |
| Physical Port Attribute     | -                                  | This parameter is unavailable for the board.                                                                                                                                 |
| ARP Aging Time (min.)       | 1 to 1440 Default: 720             | Indicates the ARP aging time of the port. After the ARP aging time expires, the equipment automatically updates dynamic ARP entries to prevent incorrect address resolution. |
| Running Status              | -                                  | This parameter is unavailable for the board.                                                                                                                                 |
| Optical Module Status       | -                                  | This parameter is unavailable for the board.                                                                                                                                 |
| Laser Interface Status      | -                                  | This parameter is unavailable for the board.                                                                                                                                 |
| Laser Transmission Distance | -                                  | This parameter is unavailable for the board.                                                                                                                                 |

Table 13-22 Flow control

| Field                          | Value                               | Description                                                                                                                                                                                                                       |
|--------------------------------|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Traffic Policing Status        | Enabled, Disabled Default: Disabled | Enables or disables traffic monitoring on the port. When you need to monitor the traffic on a port, enable the traffic monitoring function to monitor the traffic on a port in the period specified by  Traffic Policing Period . |
| Traffic Policing Period (min.) | 1 to 30 Default: 15                 | Specifies the traffic monitoring period.                                                                                                                                                                                          |

Table 13-23 Layer 2 attributes

| Field                                  | Value   | Description                                                      |
|----------------------------------------|---------|------------------------------------------------------------------|
| Port                                   | -       | Displays the virtual Ethernet port, for example, 40001(V\_ETH-1). |
| Non- Autonegotiation Flow Control Mode | -       | This parameter is unavailable for the board.                     |
| Auto-Negotiation Flow Control Mode     | -       | This parameter is unavailable for the board.                     |

| Field            | Value                       | Description                                                                                                                          |
|------------------|-----------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| Port             | -                           | Displays the virtual Ethernet port, for example, 40001(V\_ETH-1).                                                                     |
| QinQ Type Domain | 0600 to FFFF Default: 81 00 | Sets the QinQ type domain. This parameter is available only when you set Encapsulation Type in General Attributes to QinQ or 802.1Q. |

| Field           | Value                                        | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|-----------------|----------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Tag             | Tag Aware, Access, Hybrid Default: Tag Aware | Identifies the type of packets. ● Tag Aware : If the port is set to Tag aware, the port transparently transmits the packets with a VLAN ID (namely, tagged packets) and discards the packets without a VLAN ID (namely, untagged packets). At this time,  Default VLAN ID  and  VLAN Priority  are unavailable. ● Access : If the port is set to Access, the port attaches the default VLAN ID to the packets without a VLAN ID (namely, untagged packets) and discards the packets with a VLAN ID (namely, tagged packets). ● Hybrid : If the port is set to Hybrid, the port attaches the default VLAN ID to the packets without a VLAN ID (namely, untagged packets) and transparently transmits the packets with a VLAN ID (namely, tagged packets). This field is unavailable if Encapsulation Type  in  General Attributes  is set to  QinQ . |
| Default VLAN ID | 1 to 4094 Default: 1                         | Specifies the default VLAN ID of the packets that can be transmitted by the port. ● If  TAG  is set to  Access , the port discards the packets that contain the VLAN ID, but attaches the default VLAN ID to the packets that do not contain a VLAN ID and then transmits these packets. ● If  TAG  is set to  Hybrid , the port transmits the packets that contain a TAG, and attaches the default VLAN ID to the packets that do not contain a TAG and then transmits these packets.                                                                                                                                                                                                                                                                                                                                                              |

Table 13-24 Layer 3 Attributes

| Field         | Value             | Description                                                                                                                                                                                                                                                                |
|---------------|-------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| VLAN Priority | 0 to 7 Default: 0 | Specifies the class of service (CoS) when  TAG  is set to  Access  or  Hybrid . 0  indicates the lowest priority and  7 the highest. When the network is busy, data packets of higher VLAN priority are processed first and those of lower VLAN priority may be discarded. |
| SVLANs        | 1-4094            | Specifies the ID of the S-VLAN. When C-VLANs and S-VLANs are configured on the same port, this parameter must be set. This parameter can be set only when Encapsulation Type  is set to  802.1Q .                                                                          |

| Field                          | Value                 | Description                                                                                                                                                              |
|--------------------------------|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Port                           | -                     | Displays the virtual Ethernet port, for example, 40001(V\_ETH-1).                                                                                                         |
| Enable Tunnel                  | Enabled, Disabled     | After this parameter is set to  Enabled for a port, the port can identify and process MPLS labels.                                                                       |
| Max Reserved Bandwidth(kbit/s) | -                     | Specifies the max reserved bandwidth.                                                                                                                                    |
| Available Bandwidth(kbit/s)    | -                     | Displays the available bandwidth.                                                                                                                                        |
| Specify IP Address             | Manually, Unspecified | When a port carries tunnel services, or when  Port Mode  is set to  Layer 3 , set this parameter to  Manually . For other scenarios, set this parameter to Unspecified . |

| Field            | Value   | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|------------------|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| IP Address       | -       | Specifies the port IP address. This parameter is valid only when Specify IP Address  is set to  Manually . NOTE When setting the IP address for a port, ensure that the IP address is in a different network segment from the IP address of other service ports and the NE IP address, preventing service interruption from occurring or the NE from being unreachable by the NMS. For example, the IP address and subnet mask of an NE are 129.9.0.x and 255.255.0.0, respectively. This means that the NE IP address is in the 129.9 network segment. The IP address and subnet mask of a service-present port on the NE are 10.0.1.1 and 255.255.255.0, respectively. This means the port IP address is in the 10.0.1 network segment. In this situation, |
| IP Mask          | -       | you cannot assign IP addresses in the 129.9 and 10.0.1 network segments to other ports on the NE. In other words, you cannot set the IP addresses to 129.9.x.x or 10.0.1.x for other ports on the NE. Specifies the port subnet mask. This parameter is valid only when Specify IP Address  is set to  Manually . Indicates the IP address of the next hop.                                                                                                                                                                                                                                                                                                                                                                                                  |
| Next Hop Address | -       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |

Table 13-25 Advanced attributes

| Field                   | Value                  | Description                                                                                                                                                                                                                                                                                                                                                                                                                                |
|-------------------------|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| MPLS Encapsulation Mode | GFP\_ETHERNET, GFP\_MPLS | Specifies the MPLS encapsulation mode(This parameter can be set only for ODUk virtual ports and VP ports). ● GFP\_ETHERNET: GFP-F encapsulation is performed on the MPLS packets with Layer-2 Ethernet headers. ● GFP MPLS: GFP-F encapsulation is not performed on the Layer-2 Ethernet headers of packets. This encapsulation mode is defined in ITU-T G.7041 (2011) and does not support traffic classification. In  GFP MPLS  mode, the |

| Field                    | Value                       | Description                                  |
|--------------------------|-----------------------------|----------------------------------------------|
| Port                     | -                           | Displays the port name.                      |
| Port Physical Parameters | -                           | Displays physical parameters of the port.    |
| MAC Loopback             | -                           | This parameter is unavailable for the board. |
| PHY Loopback             | -                           | This parameter is unavailable for the board. |
| MAC Address              | Default: 00-00-00-00-00-0 0 | Displays the MAC address of the port.        |

| Field                                           | Value                               | Description                                                                                                                                                                                                                                                                                                                                                                                  |
|-------------------------------------------------|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Transmission Rate (kbit/s)                      | -                                   | Displays the rate for transmitting data packets.                                                                                                                                                                                                                                                                                                                                             |
| Receiving Rate (kbit/s)                         | -                                   | Displays the rate for receiving data packets.                                                                                                                                                                                                                                                                                                                                                |
| Loopback Check                                  | -                                   | This parameter is unavailable for the board.                                                                                                                                                                                                                                                                                                                                                 |
| Loopback Port Block                             | -                                   | This parameter is unavailable for the board.                                                                                                                                                                                                                                                                                                                                                 |
| Egress PIR Bandwidth (kbit/s)                   | -                                   | This parameter is unavailable for the board.                                                                                                                                                                                                                                                                                                                                                 |
| Broadcast Packet Suppression                    | Disabled, Enabled Default: Disabled | By using this parameter, you can enable or disable the broadcast packet suppression function for a port. This controls the volume of the incoming broadcast packets on a port. When the broadcast packet suppression function is enabled for a port and the volume of the incoming broadcast packets exceeds the preset threshold on the port, all incoming broadcast packets are discarded. |
| Broadcast Packet Suppression Threshold (Mbit/s) | Default: 30                         | When the broadcast packet suppression function is enabled, if the broadcast packet occupies a bandwidth that exceeds the overall bandwidth of the port x the suppression threshold, the broadcast packet is suppressed.                                                                                                                                                                      |
| Network Cable Mode                              | -                                   | This parameter is unavailable for the board.                                                                                                                                                                                                                                                                                                                                                 |
| Optical Module Type                             | -                                   | This parameter is unavailable for the board.                                                                                                                                                                                                                                                                                                                                                 |
| Synchronous Clock Enabled                       | -                                   | This parameter is unavailable for the board.                                                                                                                                                                                                                                                                                                                                                 |
| Mapping Protocol                                | GFP-F, GFP-T Default: GFP-F         | Indicates the Generic Framing Procedure (GFP) used by Ethernet services that traverse virtual ports on universal line boards.                                                                                                                                                                                                                                                                |
| Enable Bit Error Detection                      | -                                   | This parameter is unavailable for the board.                                                                                                                                                                                                                                                                                                                                                 |

| Field                                 | Value   | Description                                  |
|---------------------------------------|---------|----------------------------------------------|
| EXC Threshold for Packet Loss at Port | -       | This parameter is unavailable for the board. |
| SD Threshold fort Packet Loss at Port | -       | This parameter is unavailable for the board. |
| Band Type                             | -       | This parameter is unavailable for the board. |
| Wavelength No.                        | -       | This parameter is unavailable for the board. |

## 13.3.10 Adaptation Module

| Optical Modules                                                                                                    | App lica tion s   | Service type   | Type               | Initial Version    |
|--------------------------------------------------------------------------------------------------------------------|-------------------|----------------|--------------------|--------------------|
| 100G CFPT65(Metro,SDFEC2,Coh erent wDCM,Tunable,expanded C Band,-3dBm-2dBm,-18dBm, 50GHz,LC)-High Optical Power    | Line - Side       | OTU4           | Plugga ble modul e | V100R009C0 0SPC700 |
| CFP,4*25Gb/s(1310nm Band),103.125Gb/s &111.81Gb/s-100G Dual Rates,-1.3dBm, 4.5dBm,-8.6dBm,Straight LC,SMF,OMA,10km | Line - Side       | OTU4           | Plugga ble modul e | V100R009C0 0SPC700 |
| 100G CFPT5U(ULH +,SDFEC2,Coherent,Tunable ,Extended C Band,-5dBm,-1dBm,-16dBm ,50GHz,LC)                           | Line - Side       | OTU4           | Plugga ble modul e | V100R009C0 0SPC700 |
| 100G CFPT69(SH,SDFEC2,Cohere nt wDCM,Tunable,expanded C Band,-2dBm-2dBm,-27dBm, 50GHz,LC)-High Optical Power       | Line - Side       | OTU4           | Plugga ble modul e | V100R009C0 0SPC700 |

| Optical Modules                                                                          | App lica tion s   | Service type   | Type               | Initial Version    |
|------------------------------------------------------------------------------------------|-------------------|----------------|--------------------|--------------------|
| 100G CFPT51(SLH,SDFEC2,Cohere nt,Tunable,Extended C Band,-5dBm,-1dBm,-16dBm ,Fixed)      | Line - Side       | OTU4           | Plugga ble modul e | V100R009C0 0SPC700 |
| 100G CFPT61(ULH,SDFEC2,Coher ent wDCM,Tunable,Extended C Band,-5dBm,-1dBm,-16dBm ,Fixed) | Line - Side       | OTU4           | Plugga ble modul e | V100R009C0 0SPC700 |
| 100G CFPA51(SLH,SDFEC2,Coher ent,Tunable,Extended C Band,-5dBm-0dBm,-16dBm, Fixed)       | Line - Side       | OTU4           | Plugga ble modul e | V100R021C1 0SPC300 |
| 100G CFPA62(LH,SDFEC2,Cohere nt wDCM,Tunable,Extended C Band,-5dBm-0dBm,-16dBm, Fixed)   | Line - Side       | OTU4           | Plugga ble modul e | V100R021C1 0SPC300 |

<!-- image -->

If the board is equipped with the 100G CFPT65(Metro,SDFEC2,Coherent wDCM,Tunable,expanded C Band,-3dBm-2dBm,-18dBm,50GHz,LC)-High Optical Power, 100G CFPT69(SH,SDFEC2,Coherent wDCM,Tunable,expanded C Band,-2dBm-2dBm,-27dBm, 50GHz,LC)-High Optical Power, 100G CFPT5U(ULH+,SDFEC2,Coherent,Tunable,Extended C Band,-5dBm,-1dBm,-16dBm,50GHz,LC) optical module on the WDM side, the board can work with the single-fiber bi-directional OADM boards (SBMx boards).

100G CFPT69(SH,SDFEC2,Coherent wDCM,Tunable,expanded C Band,-2dBm-2dBm,-27dBm, 50GHz,LC)-High Optical Power optical module is applicable only to the single-span scenario without OAs. It does not support wavelength dropping from RDU (for example, wavelength dropping from WSMD4), but supports signal transmission with 10G signals.

When 100G CFPT5U(ULH+,SDFEC2,Coherent,Tunable,Extended C Band,-5dBm,-1dBm,-16dBm,50GHz,LC), 100G CFPT65(Metro,SDFEC2,Coherent wDCM,Tunable,expanded C Band,-3dBm-2dBm,-18dBm,50GHz,LC)-High Optical Power, 100G CFPT69(SH,SDFEC2,Coherent wDCM,Tunable,expanded C Band,-2dBm-2dBm,-27dBm, 50GHz,LC)-High Optical Power, 100G CFPT51(SLH,SDFEC2,Coherent,Tunable,Extended C Band,-5dBm,-1dBm,-16dBm,Fixed) or 100G CFPT61(ULH,SDFEC2,Coherent wDCM,Tunable,Extended C Band,-10dBm-4dBm,-18dBm,Fixed)-High Optical Power works together with the WDM device, the working wavelength ranges from 1529 nm to 1560 nm.

There is a margin between the input power low alarm threshold and the receiver sensitivity and a margin between the input power high alarm threshold and the overload point. This ensures that the system can report an input power low alarm before the actual input power reaches the receiver sensitivity or an input power high alarm before the actual input power reaches the overload point.

## 13.3.11 Board Specifications

## Mechanical Specifications

| Board   | Item                                          | Unit   | Value                |
|---------|-----------------------------------------------|--------|----------------------|
| TNZ8NS4 | Dimensions (H x W x D)                        | mm     | 40.10×193.80 ×205.90 |
|         | Dimensions (H x W x D)                        | in.    | 1.58×7.64×8.1 1      |
|         | Weight                                        | kg     | 1.75                 |
|         | Weight                                        | lb.    | 3.86                 |
|         | Typical Power Consumption (Line mode)         | W      | 82.7                 |
|         | Typical Power Consumption (Regeneration mode) | W      | 79.6                 |
|         | Maximum Power Consumption (Line mode)         | W      | 88.6                 |
|         | Maximum Power Consumption (Regeneration mode) | W      | 85.7                 |
