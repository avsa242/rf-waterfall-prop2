# rf-waterfall-prop2
--------------------

This is a P2X8C4M64P/Propeller 2-based RF spectrogram/waterfall application utilizing commonly-available ISM-band packet radio ICs.


## Salient Features

* Supported transceivers: __Sub-GHz__: CC1101, SX1231. __2.4GHz__: CC2500
* Display a waterfall of band radio is tuned to
* Change LNA (CC1101, CC2500, SX1231), DVGA gains (CC1101, CC2500)
* Change receiver bandwidth (CC1101, CC2500, SX1231)
* Change IF (CC1101, CC2500)
* Change color scale offset/reference level to improve display contrast
* Change waterfall span
* Change base freq


## Requirements

* [p2-spin-standard-library](https://github.com/avsa242/p2-spin-standard-library)
* [gui-spin](https://github.com/avsa242/gui-spin)
* [cc1101-spin](https://github.com/avsa242/cc1101-spin) for CC1101 support
* [cc2500-spin](https://github.com/avsa242/cc2500-spin) for CC2500 support
* [sx1231-spin](https://github.com/avsa242/sx1231-spin) for SX1231 support
* Compatible RF module (CC1101, CC2500, SX1231)
* NOTE: Module must allow direct/low-level programming of the transceiver IC. There exist some modules that are intended to be used as wireless UARTs/"wireless serial ports" - these won't work.


# Compiler Compatibility

| Processor | Language | Compiler               | Backend      | Status                |
|-----------|----------|------------------------|--------------|-----------------------|
| P1        | SPIN1    | FlexSpin (7.6.0)       | Bytecode     | Not supported         |
| P1        | SPIN1    | FlexSpin (7.6.0)       | Native/PASM  | Not supported         |
| P2        | SPIN2    | FlexSpin (7.6.0)       | NuCode       | OK                    |
| P2        | SPIN2    | FlexSpin (7.6.0)       | Native/PASM2 | OK                    |

(other versions or toolchains not listed are __not supported__, and _may or may not_ work)


## Limitations

* Very early in development - may malfunction, or outright fail to build
* Crude - simply sweeps frequencies and reads the radio's RSSI register for that frequency. Not optimized and doesn't display absolute power levels

