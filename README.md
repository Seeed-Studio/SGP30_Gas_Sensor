SGP30_Gas_Sensor    [![Build Status](https://travis-ci.com/Seeed-Studio/SGP30_Gas_Sensor.svg?branch=master)](https://travis-ci.com/Seeed-Studio/SGP30_Gas_Sensor)
==================
A arduino example for SGP30_Gas_Sensor,Measurement of TVOC and CO2
------------------------------------------------------------------
***
Introduction of sensor  
----------------------
The SGP30 is a digital multi-pixel gas sensor designed foreasy integration into air purifier,
demand-controlledventilation, and IoT applications. Sensirion’s CMOSens®technology offers a 
complete sensor system on a single chip featuring a digital I2C interface, a temperature 
controlled micro hotplate, and two preprocessed indoor air quality signals. As the first 
metal-oxide gas sensor featuring multiple sensing elements on one chip, the SGP30 provides 
more detailed information about the air quality.  

***  
Usage:  
===========
Download all the source files and open examples/ * / *.ino in arduino IDE.
Compile and download and run it on a arduino board.

Notice:
----------
* **The SGP30 uses a dynamic baseline compensation algorithm and on-chip calibration parameters to provide two
complementary air quality signals. The baseline should be stored in EEPROM.When there is no baseline value
in EEPROM at the first time power-ON or the baseline record is older than seven days.The sensor has to run
for 12 hours until the baseline can be stored.
You can refer to program flow chart blow**  
![baseline operation](https://github.com/linux-downey/SGP30_Gas_Sensor/blob/master/pictures/Get%20baseline%20program%20flow%20chart%20.png)  
* **The H2_Signal and Ethanol_signal,Both signals can be used to calculate gas concentrations c relative to a reference concentration cref by
ln(C/Cref)=(Sref-Sout)/a
with a = 512, sref the H2_signal or Ethanol_signal output at the reference concentration, and sout = Sout_H2 or Sout = Sout_EthOH.**  
* **For more accurate measurement,You can set the abslute humidity compensation,Defalt value is 11.57g/m3,A little troublesome is
that you should get relatively humidity value of environment from another way,Because there is no humidity measurement part integrated in SGP30..
![Humidity caculation formula](https://github.com/linux-downey/SGP30_Gas_Sensor/blob/master/pictures/absolute%20humidity%20with%20the%20formula.png)  
Luckly, It's not much neccessary in a normal situation**  
* ***All relevant example is in examples/,To get more detail***  

reference:  
============
* [SGP30 Datasheet](https://www.sensirion.com/fileadmin/user_upload/customers/sensirion/Dokumente/9_Gas_Sensors/Sensirion_Gas_Sensors_SGP30_Datasheet_EN.pdf)  
* [Driver Integration](https://www.sensirion.com/fileadmin/user_upload/customers/sensirion/Dokumente/9_Gas_Sensors/Sensirion_Gas_Sensors_SGP30_Driver-Integration-Guide_HW_I2C.pdf)  

Or you can also visit [sensirion|home](https://www.sensirion.com/cn/environmental-sensors/gas-sensors/multi-pixel-gas-sensors/) to get more information about SGP30  


***
This software is written by downey  for seeed studio<br>
Email:dao.huang@seeed.cc
and is licensed under [The MIT License](http://opensource.org/licenses/mit-license.php). Check License.txt for more information.<br>

Contributing to this software is warmly welcomed. You can do this basically by<br>
[forking](https://help.github.com/articles/fork-a-repo), committing modifications and then [pulling requests](https://help.github.com/articles/using-pull-requests) (follow the links above<br>
for operating guide). Adding change log and your contact into file header is encouraged.<br>
Thanks for your contribution.

Seeed Studio is an open hardware facilitation company based in Shenzhen, China. <br>
Benefiting from local manufacture power and convenient global logistic system, <br>
we integrate resources to serve new era of innovation. Seeed also works with <br>
global distributors and partners to push open hardware movement.<br>


[![Analytics](https://ga-beacon.appspot.com/UA-46589105-3/CAN_BUS_Shield)](https://github.com/igrigorik/ga-beacon)
