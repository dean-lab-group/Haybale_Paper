#

## Abstract
The agricultural industry is undergoing a technological revolution as devices reserved for multinational agricultural corporations become available to the local family-owned farm or ranch.
By creating a low-cost environmental sensing platform based on PCB sensor technology, we are able to create a globally connected Agricultural Internet Of Things (AIOT) device that detects and alerts the farmer/rancher of hazardous environmental conditions.
Our current research continues in monitoring environmental conditions inside hay bales.
Hay bales spontaneously combust when baled hay with excessive moisture content, creates a habitable and nutrient rich environment for thermophilic and mesophilic bacteria.
This combustion is due to the growth of these microorganisms that flourish in moist and warm habitats and produce a combustable environment at temperatures as low as 180$\deg$F.

The solution presented is a low-power, low-cost, internet-connected device inserted into the bale that monitors environmental conditions (temperature and moisture content).
The device automatically monitors the moisture and temperature inside a hay bale and the user receives alerts on their smartphone when dangerous combustion-triggering conditions exist.
A PCB-based moisture content sensor and a discrete temperature sensor interfaces with a microcontroller that connects to the internet or directly to a user’s cellphone when in range.
With the potential low cost of the electronics stack, a variety of other applications are possible as well, such as monitoring soil, hen houses, remote feedlots, and any other locations where temperature and moisture content information is useful.
Collecting information and data mining can also lead to better understanding hay bale combustion, both from a scientific perspective and for the farmer/rancher to integrate into finding ideal baling weather conditions.
Software on the microcontroller handles the  calibration of the fringing field PCB-based moisture content sensor and thermistor-based temperature sensor.
The software architecture is designed so that new calibration data can be pushed to devices remotely by the developer.
Calibration parameters are stored in EEPROM on the sensor platform, allowing updates and modification to the sensor operation in the field without requiring a complete firmware reload.

## Introduction
In the previous paper, information was presented that demonstrated this sensor's ability to alert farmers of possible hay bale combustion from thermophilic bacteria colonies in wet hay. Further refinement of the sensor suite found a nonlinear correlation between the relaxation oscillator frequency output from the temperature sensing thermistor subsystem and the temperature from an independent thermocouple. Furthermore, heavy noise prevented accurate readings from being found. Implementing a moving average filter increased the accuracy of temperature readings.

## Background
As previously discussed \ref{haybale1}, high losses to farm equipment and possible loss of life creates a real market demand for being able to measure the moisture content inside a hay bale. Current commercial offerings available require a user to insert a probe into the hay bale manually whenever moisture and temperature conditions need to be determined.

## Requirements and Design

## Calibration
### Temperature
To calibrate the thermistor/relaxation oscillator circuit, the output frequency was compared to that of a MAX 6675 thermocouple board connected to an Arduino microcontroller used for datalogging purposes. The thermocouple and the sensor suite was inserted into approximately \degC water which was allowed to cool to room temperature. By recording the relaxation oscillator frequency every 5 seconds and comparing that to the temperature from the thermocouple, a correlation between 100% moisture, with varying temperature was achieved. The data shown in Figure \ref{noisy_temp} revealed that there is a lot of noise and variation in the relaxation oscillator frequency at a specific temperature. However, the relaxation oscillator frequency were consistently varying around a midpoint. Using a moving average filter, the average frequency at a specific temperature could be determined. This is possible because the change in temperature as a function of time is small compared to the frequency of the relaxation oscillator.

The outcome of this analysis revealed that the output of the relaxation oscillator as a function of temperature is nonlinear in nature and not linear as previously assumed. Using the Numeric Python library, a polynomial fit was generated on the calibration dataset. The dataset contained about 5000 datapoints collected from the relaxation oscillator sampling and the thermocouple. The temperatures were also compared with a second thermocouple. Using a 2nd order polynomial function, the thermistor could be calibrated to show a temperature within 5 degrees of the thermistor temperature.

### Moisture
Due to limited access to a proper environmental chamber for calibrating 

## User interface
The user interface was designed to allow a farmer to easily see the temperature moisture content in the bale (see Figure \ref{fig:app_gui})


## Quality Control

## Conclusion
