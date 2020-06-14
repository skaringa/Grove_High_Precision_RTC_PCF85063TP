# Grove - High Precision RTC_PCF85063TP 
Grove - High Precision RTC is based on PCD85063TP, it's usage is almost the same with ds1307.

<img src=https://statics3.seeedstudio.com/seeed/img/2016-11/1GtDOEsSVtk0i3pa5JBXOSTb.jpg width=300><img src=https://statics3.seeedstudio.com/seeed/img/2016-11/brK2Tu9LnaVBztZnmbP8x0we.jpg width=300>

[Grove - High Precision RTC](https://www.seeedstudio.com/Grove-High-Precision-RTC-p-2741.html)

Grove - High Precision RTC based on the clock chip PCF85063TP which is a CMOS Real-Time Clock (RTC) and calendar optimized for low power consumption. An offset register allows fine-tuning of the clock. All addresses and data are transferred serially via the I2C bus and the maximum bus speed is 400 kbit/s.

For more information please visit [wiki page](http://wiki.seeedstudio.com/Grove_High_Precision_RTC/).

This is an extended version that fixes some bugs and adds the ability to control the interrupts sent by the PCF85063TP.

## Methods

* void startClock(void);
* void stopClock(void);
* void setTime(void);
* void getTime(void);
* void setcalibration(int mode, float Fmeas);
  - mode 0 - offset is made once every 2 hours
  - mode 1 - offset is made once every 4 minutes
  - Fmeas - real clock frequency you detcet
* uint8_t readCalibrationReg(void);
  - read offset register at 0x02
* uint8_t calibratBySeconds(int mode, float offset_sec);
  - offset_sec - need a long time running RTC and work out the offset by one second 
* uint8_t setInterrupt(bool MI, bool HMI);
  - enable or disable the minute (MI) or half-minute (HMI) interrupt
* uint8_t readInterruptReg();
  - read register Control_2 at 0x01
* void reset();
* void fillByHMS(uint8_t _hour, uint8_t _minute, uint8_t _second);
* void fillByYMD(uint16_t _year, uint8_t _month, uint8_t _day);
* void fillDayOfWeek(uint8_t _dow);

----

This software is licensed under [The MIT License](http://opensource.org/licenses/mit-license.php). Check License.txt for more information.<br>


Seeed Studio is an open hardware facilitation company based in Shenzhen, China. <br>
Benefiting from local manufacture power and convenient global logistic system, <br>
we integrate resources to serve new era of innovation. Seeed also works with <br>
global distributors and partners to push open hardware movement.<br>


[![Analytics](https://ga-beacon.appspot.com/UA-46589105-3/Grove_High_Precision_RTC_PCF85063TP)](https://github.com/igrigorik/ga-beacon)

