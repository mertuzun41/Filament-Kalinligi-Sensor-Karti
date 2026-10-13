[Türkçe](README.md) | **English**

# Filament Thickness Measurement Sensor Board

A sensor board I developed at DYROBX Robotics to monitor filament thickness (diameter). The project combines analog data acquisition from a Hall sensor, analog-to-digital conversion, microcontroller-based processing, and communication with the main control system on a single PCB.

**Status:** The board design, PCB fabrication, and component assembly are complete. The board has been brought up and is operational.

## Project Goal

To develop a compact electronic board that reads sensor data from a filament diameter measurement mechanism and connects to the main control system. The design brings together the analog measurement chain, embedded control, power regulation, and communication interfaces.

## Hardware Architecture

| Function | Implementation |
|---|---|
| Microcontroller | ESP32-C3 |
| Sensing | DRV5056A3 analog Hall sensor |
| Analog-to-digital conversion | MCP3221, 12-bit ADC with an I²C interface |
| Signal conditioning | RC filter on the Hall sensor output |
| Communication | THVD1420-based RS485 interface |
| Power supply | USB-C or external 5 V input; onboard 3.3 V regulation |
| Service and programming | USB-C, BOOT and RESET buttons |
| Design tool | KiCad |

The Hall sensor's analog output is filtered and read through the external ADC. The ESP32-C3 processes the digitized data, while the RS485 interface provides communication with the main control system. Conversion of sensor readings into filament diameter values depends on the measurement mechanism and its calibration.

## My Contribution

- Created the schematic design, including the analog measurement, microcontroller, power supply, and communication blocks.
- Completed the PCB placement and routing.
- Assembled the components on the fabricated PCB and brought the board into operation.

This completed project took a sensor board from schematic design to working hardware, combining my experience in analog electronics, PCB design, and board bring-up.

## Assembled Board

<table>
  <tr>
    <th>Front side and component assembly</th>
    <th>Back side</th>
    <th>Hall sensor mounting</th>
  </tr>
  <tr>
    <td><a href="kart-on-yuz.jpg"><img src="kart-on-yuz.jpg" alt="Front side of the assembled filament sensor board" width="280"></a></td>
    <td><a href="kart-arka-yuz.jpg"><img src="kart-arka-yuz.jpg" alt="Back side of the filament sensor board" width="280"></a></td>
    <td><a href="hall-sensor-montaji.jpg"><img src="hall-sensor-montaji.jpg" alt="Hall sensor mounted on the board" width="280"></a></td>
  </tr>
</table>

Click a photo to open the full-size image.

## Repository Contents

- `README.md`: Project overview, hardware architecture, and my contribution in Turkish.
- `README.en.md`: English version of the project overview.
- `kart-on-yuz.jpg`: Front side of the assembled board.
- `kart-arka-yuz.jpg`: Back side of the board.
- `hall-sensor-montaji.jpg`: Hall sensor mounting.

[My other engineering projects](https://github.com/mertuzun41/Projeler)
