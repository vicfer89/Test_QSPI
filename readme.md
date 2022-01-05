# Test_QSPI

Tests para memoria QSPI W25Q128

## Información sobre configuración y proyecto:

### Uso como memoria SPI normal:

- [Video Youtube](https://www.youtube.com/watch?v=AWUgv49JRuw)
- [Librería empleada](https://github.com/NimaLTD/w25qxx)

### Uso como memoria QSPI:

- [Video Youtube](https://www.youtube.com/watch?v=xIfh_uYy-OU)
- [Información adicional](https://githubhelp.com/Crazy-Geeks/STM32-W25Q-QSPI)

### Información general de memoria W25Qxx

- [Datasheet](https://www.pjrc.com/teensy/W25Q128FV.pdf)
- [Pinout Nucleo F746G](https://os.mbed.com/platforms/ST-Nucleo-F746ZG/)

## Configuraciones:

### Pinout para Nucleo-F746G:

- w25qxx_vcc -> Nucleo_3V3 (CN8 3V3)
- w25qxx_gnd -> Nucleo_GND (CN8 GND)
- w25qxx_CS -> Nucleo_PB9 (CN7 D14)
- w25qxx_CLK -> Nucleo_PA5 (CN7 D13) -> SPI1_SCK
- w25qxx_DO -> Nucleo_PA6 (CN7 D12) -> SPI1_MISO
- w25qxx_DI <- Nucleo_PA7 (CN7 D11) <- SPI1_MOSI

### Configuracion SPI:

- Tamaño de datos: 8 Bits
- Primer Bit: MSB First
- Preescaler: 8 (13.5 Mbit/s máximo probado)
- CPOL: Low
- CPHA: 1 Edge