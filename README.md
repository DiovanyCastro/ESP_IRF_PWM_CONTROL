

# Example for `pca9685` driver

## What it does

OBS: A CONFIGURAÇÃO DEFAULT É MUITO ALTA, RECOMENDO ENTRE 600 À 800

The example configures a `pca9685` device. It sets frequency to
`CONFIG_EXAMPLE_PWM_FREQ_HZ` (1500 by default), shows the actual frequency. 
The PWM values for channels 0 and 3 start to change continuously.

OBS: AS DUAS CONFIGURAÇÕES ABAIXO ESTÃO COMO #DEFINE. EU CREIO SER MAIS VALIDO UNSIGNED CHAR PARA LED0 E LED3

* Channel 0 (`LED0`): from 0 to 4096
* Channel 3 (`LED3`): from 4096 down to 0

## Wiring

Connect each of `LED0` and `LED3` pins of `pca9685` to an LED and a resistor.

OBS: DEPENDENDO DA VERSAO DO ESP VOCÊ TIVER, DEVERÁ TROCAR OS GPIO DE COMUNICAÇÃO.OS RECOMENDADOS NA TABELA ABAIXO NÃO SÃO 100% CONFIAVEIS

Connect `SCL` and `SDA` pins to the following pins with appropriate pull-up
resistors.

| Name | Description | Defaults |
|------|-------------|----------|
| `CONFIG_EXAMPLE_I2C_MASTER_SCL` | GPIO number for `SCL` | "5" for `esp8266`, "6" for `esp32c3`, "19" for `esp32`, `esp32s2`, and `esp32s3` |
| `CONFIG_EXAMPLE_I2C_MASTER_SDA` | GPIO number for `SDA` | "4" for `esp8266`, "5" for `esp32c3`, "18" for `esp32`, `esp32s2`, and `esp32s3` |
