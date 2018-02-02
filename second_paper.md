#

## Abstract
The agricultural industry is undergoing a technological revolution as devices reserved for multinational agricultural corporations become available to the local family-owned farm/ranch.
By creating a low cost environmental sensing platform, based on PCB sensor technology, we are able to create a globally connected Agricultural Internet Of Things (AIOT) device that detects and alerts the farmer/rancher of preset environmental conditions.
Our current research continues in monitoring environmental conditions inside hay bales.
Hay bales spontaneously combust when baled hay with excessive moisture present creates a habitable and nutrient rich environment for thermophilic and mesophilic bacteria.
This combustion is due to growth of thermophilic microorganisms that flourish in moist and warm habitats.

A low-power, low-cost internet-connected device inserted into the bale and monitors environmental conditions (temperature and moisture content). An end-user monitors the moisture and temperature inside a hay bale and receive alerts on their smartphone when dangerous conditions exist that could trigger combustion. A PCB-based moisture content sensor and a discrete temperature sensor interfaces with a microcontroller that connects to the internet or directly to a user’s cellphone when in range. With the low cost of the electronics stack, a variety of other applications are possible as well, such as monitoring soil, hen houses, remote feedlots, and any other location where temperature and moisture content information is useful. Collecting information and data mining can also lead to better understanding hay bale combustion, both from a scientific perspective and for the farmer/rancher to integrate into finding ideal baling weather conditions. Software on the microcontroller handles the  calibration of the fringing field PCB-based moisture content sensor and thermistor-based temperature sensor. This architecture allows new calibration data to be pushed to devices remotely by the developer. Calibration parameters are stored in EEPROM on the sensor platform, allowing modification to the sensor operation without requiring a complete firmware reload.

## Introduction
In the previous paper, information was presented that demonstrated the sensor suit's ability to alert farmers of possible hay bale combustion from thermophilic bacteria colonies in wet hay. Further refinement of the sensor suite found nonlinear correlation between the relaxation oscillator frequency output from the temperature sensing thermistor subsystem and the temperature from an independent thermocouple.

## Background

## Requirements and Design

## Calibration
To calibrate the thermistor/relaxation oscillator circuit, the output frequency was compared to that of a MAX{????} thermocouple connected to an Arduino microcontroller used for datalogging purposes.



## Quality Control

## Conclusion
