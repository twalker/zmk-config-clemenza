# Clemenza ZMK configuration

Configuration for Clemenza, a 41 key hand-wired keyboard with integrated trackball.


### TODO

- [x] Remove encoder support
- [x] Adapt pinout for cols and rows
- [x] Adjust key matrix for 38 keys
- [x] Add [sensor driver](https://github.com/inorichi/zmk-pmw3610-driver) and [configure pointing device](https://zmk.dev/docs/development/hardware-integration/pointing)
- [x] Add nice!view adapter and enable
- [x] Update keymap to the same as QMK, but with BT keys on macro layer
- [ ] Potentially add build guide

### References
- [New shield ZMK documentation](https://zmk.dev/docs/development/hardware-integration/new-shield)
- [Clemenza](https://www.imdb.com/title/tt0068646/characters/nm0144710/?ref_=tt_cst_c_4)

- [pmw3610 Pinout reddit](https://www.reddit.com/r/ErgoMechKeyboards/comments/1h0zy8n/help_which_nicenane_pins_to_connect_to_this/#lightbox)
- [pmw3610-pcb](https://github.com/siderakb/pmw3610-pcb)
- [zmk-pmw3610-driver](https://github.com/inorichi/zmk-pmw3610-driver)


### pinout for display and sensor

Default Nice!View pinout:
```
CS   = P0.06 / D1
SCL  = P0.17 / D2
MOSI = P0.20 / D3
```

Custom pinout:
```
CS   = D14 / P1.11
SCL  = D16 / P0.10
MOSI = D10 / P0.09
```

Best guess pmw3610 pinout:
```
SDIO (moso/miso) = P0.17
SCLK (sck)       = P0.08
nCS (gpios)      = P0.20
Mot (irq)        = P0.06

```


Moved pmw3610 pinout to accomodate display:
```

SDIO (moso/miso) = P0.22 / D4
SCLK (sck)       = P0.24 / D5
nCS (gpios)      = P1.00 / D6
Mot (irq)        = P0.11 / D7
```


## Wiring diagram

![wiring diagram](./clemenza_wiring-wireless.svg)
