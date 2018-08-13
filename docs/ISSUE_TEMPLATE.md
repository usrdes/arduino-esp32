### Hardware:
Board:							ESP32 Dev Module

Core Installation/update date:			12/Aug/2018

IDE name:							Arduino IDE 1.8.6

Flash Frequency:					80Mhz

PSRAM:                Enabled

Upload Speed:						115200


### Description:
Any Arduino sketch that depends on CPU frequency of 160 MHz or 80 MHz is not working,
because the current releae is setup for CPU freq on only 240 MHz.

Bigger issue is: There appears no way to set the CPU frequency.


### Sketch:
Try this: 
https://github.com/earlephilhower/ESP8266Audio

### Debug Messages:
Other than the i2c compile time issue:

C:\Users\....\Documents\Arduino\hardware\espressif\esp32\libraries\ESP8266Audio\src\AudioOutputI2S.cpp:191:10: warning: 'int i2s_push_sample(i2s_port_t, const void*, TickType_t)' is deprecated [-Wdeprecated-declarations]

   return i2s_push_sample((i2s_port_t)portNo, (const char *)&s32, 0);
   
The Audio playback is obviously much faster than the song should be played.


