## The problem: ESP32 (ESP32-WROOM-32) ADC with resistive moisture sensor not working in MicroPython



```
from machine import Pin, ADC
adc = ADC(Pin(32))
adc.atten(ADC.ATTN_11DB)
adc.width(ADC.WIDTH_12BIT)
adc.read() # this block of code once worked and produced 4095 when no moisture and lower when moist
```

With the kind of [resistive soil moisture sensor seen in this DFRobot blog](https://www.dfrobot.com/blog-1156.html) there are two issues:
* [ADC on ESP32 in MicroPython has internal reference voltage of 1.1V](https://docs.micropython.org/en/latest/esp32/quickref.html#adc-analog-to-digital-conversion) and the moisture sensor produces 3.2V as standard when there is no moisture (a bit high)
* The ADC is distorted by WLAN/WiFi power draw.


# Problem behaviour

As I said that code block once worked and produced sensible `adc.read()` values of 4095 when dry and 2 to 3 thousand when wet. But that was an exception.

# Solution

Using two 4.7k resistors between the A0 output of the moisture sensor and ground the voltage between the last resistor and ground is above 0.780V and when there is moisture 0.670V (approx - when measured by multimeter).

```
from machine import Pin, ADC
adc = ADC(Pin(27))
adc.read_uv() # gave 820000 when no moisture
```
So reducing the voltage, having WiFi disconnected and a new pin together resulted in reliable readings.
