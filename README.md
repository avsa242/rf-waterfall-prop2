# RF-Waterfall
--------------

This is a P2X8C4M64P/Propeller 2 application that displays power levels received by a packet radio in the frequency domain as a "waterfall." It utilizes an ISM-band transceiver IC. Currently supported ICs: CC1101

## Salient Features

* Display a waterfall of band radio is tuned to
* Change LNA, DVGA gains
* Change color scale offset to improve display contrast

## Requirements

* P2 rev B or newer silicon. Default clock is 160MHz, though 250MHz or greater is strongly recommended.

## Compiler Compatibility

* FastSpin (tested with 4.1.4-beta)

## Limitations

* Very early in development - may malfunction, or outright fail to build
* Crude - simply sweeps frequencies and reads the radio's RSSI register for that frequency. Not optimized and doesn't display absolute power levels

## TODO

- [ ] Add some basic controls (e.g., base freq, RX BW, gain, etc)
- [ ] Add some more instrumentation (display various current radio settings)
- [ ] Add support for other radios (CC2500, SX1231, SX1276, etc)
- [ ] Add support for demodulation
- [ ] Save demodulated data to SD
