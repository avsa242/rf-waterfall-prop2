# RF-Waterfall
--------------

This is a P2X8C4M64P/Propeller 2 application that displays power levels received by a packet radio in the frequency domain as a "waterfall." It utilizes one of a supported ISM-band transceiver IC.

## Salient Features

* Supported transceivers: CC1101, CC2500, SX1231
* Display a waterfall of band radio is tuned to
* Change LNA (CC1101, CC2500, SX1231), DVGA gains (CC1101, CC2500)
* Change receiver bandwidth (CC1101, CC2500, SX1231)
* Change IF (CC1101, CC2500)
* Change color scale offset/reference level to improve display contrast
* Change waterfall span
* Change base freq

## Requirements

* P2 rev B or newer silicon. 250MHz or greater clock is strongly recommended (default is 250MHz)
* Compatible RF module
* NOTE: Module must allow direct/low-level programming of the transceiver IC. There exist some modules that are intended to be used as wireless UARTs/"wireless serial ports" - these won't work.

## Compiler Compatibility

* FastSpin (tested with 4.1.4)

## Limitations

* Very early in development - may malfunction, or outright fail to build
* Crude - simply sweeps frequencies and reads the radio's RSSI register for that frequency. Not optimized and doesn't display absolute power levels
* Staircase effect seen when signals significantly above noise floor are seen - i.e., they don't appear consistently at the same frequency, even if they actually are (optimization? Transceiver limitation?)

## TODO

- [x] Add some basic controls (e.g., base freq, RX BW, gain, etc)
- [x] Add some more instrumentation (display various current radio settings)
- [ ] Add peak hold/reset
- [ ] Add marker(s)
- [x] Add support for CC1101
- [x] Add support for SX1231
- [ ] Add support for SX1276
- [ ] Add support for SX1280
- [x] Add support for CC2500
- [ ] Add support for SI4463
- [ ] Add support for demodulation
- [ ] Save screenshot to SD
- [ ] Save history to SD
- [ ] Save demodulated data to SD
- [ ] Change base frequency to center frequency (likely more familiar coming from PC-based SDR software)
- [ ] Add reference level indicator to color scale
