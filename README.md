# Tech Fair 2025 workshop project

This repository contains the project files for the 2025 Tech Fair workshop on embedded development with Tabnine.

## Project Overview

We modify an existing desktop GUI application (Lena) to support the use of input from an externally-connected humidity, temperature and pressure sensor (Bosch BME280). We then refactor the application to support a second high-precision barometric pressure sensor (Bosch BMP390).

Project demonstrates:

- Tabnine in hardware development use cases
- leveraging complex prompting strategies, such as guide and rule files
- agent workflows
- MCP integration
- custom MCP server construction and configuration

### Hardware

- Raspberry Pi 4b, 4GB
- Adafruit Stemma Pi board
- Adafruit BMP390 QT
- Adafruit BME280 QT
- Freenove 5" DSI touchscreen
- 2x JST SH 4-pin cables 50mm 
- 1 FPC display connector cable
- 1 Canakit Raspberry Pi power supply with inline power switch
- 1 64GB microsd card

## Project starting state

This repository contains the project starting state:

- Raspberry Pi OS is installed, updated and configured
- Initial version of Lena is created with GUI scaffold but no sensor API or input
- Project guide files are created in `.tabnine` directory
    - project has been described, but no rules or MCP integrations have been defined

## Project final state

The project final state repository may be found [here](#). The final state of the includes:

- Lena is fully connected to both BMP390 and BME280 sensors through the sensor API 
- Lena displays sensor readings in the GUI when launched
- MCP server for PDF to Markdown parsing is created and configured for use in `.tabnine/MCP.md` 
    - Sensor datasheets have been parsed from PDF to Markdown for use with prompting
- Rules to guide Tabnine have been created for use in `.tabnine/rules.md`
- Prompts to generate the final code have been defined in `.tabnine/prompts.md`

## Tabnine features utilized

Many Tabnine features are leveraged through the course of this project, including:

- Remote repository connections to bring in context from outside of the workspace
- Agent workflows
- Agent tool calling
    - MCP
    - external web search
- Custom system prompts and rules
