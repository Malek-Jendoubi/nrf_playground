.. _blinky-sample:

Blinky
######

Overview
********

Requirements
************

Modifications concerning nrf52_feather
**************************************
How to ADD debugging to a nrfconnect project on feather nrf52:

1. Change uart0_default and uart0_sleep, group 1 to:
* UART_TX = P0.14
* UART_RX = P0.15

1. ADD Code to prj.config:
* CONFIG_LOG=y
* CONFIG_USE_SEGGER_RTT=y
* or change kconfig from GUI (logging->enable logging/segger)

3. Include logging library 
* #include <zephyr/logging/log.h>

4. Register Console
* LOG_MODULE_REGISTER(Less4_Exer2,LOG_LEVEL_DBG);

Building and Running
********************

Adding board support
********************