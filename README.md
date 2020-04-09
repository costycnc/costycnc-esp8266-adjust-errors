# costycnc-esp8266-adjust-errors

copied from https://sites.google.com/site/esp12wifi/edit-esp-basic

WiFi.mode(WIFI_STA);
  WiFi.begin(ssid, password);

--
 WiFi.mode(WIFI_STA);
    WiFiMulti.addAP("SSID", "PASSWORD");

.........................................................

WiFi.mode(WIFI_AP);
  WiFi.softAPConfig(apIP, apIP, IPAddress(255, 255, 255, 0));
  WiFi.softAP("DNSServer CaptivePortal example");

...............................................................



Arduino 1.8.5
insert in classes.h

void PrintAndWebOut(String itemToBePrinted); 
String evaluate(String expr); 
void SetMeThatVar(String VariableNameToFind, String NewContents, int format);
String VarialbeLookup(String VariableNameToFind);

source https://www.esp8266.com/viewtopic.php?f=45&t=12839
---------------------------------------------------------------------------------------------------
insert library from esp basic source to mydocuments\arduino\library
and remove websockets from mydocuments\arduino\library (i not try yet with wesocket)
...................................................................................................................
download and install arduino 1.6.5 from here version 2.0.0-rc1
https://www.arduino.cc/en/Main/OldSoftwareReleases#00xx

install esp package like here
http://esp8266.github.io/Arduino/versions/2.0.0/doc/installing.html
http://arduino.esp8266.com/stable/package_esp8266com_index.json

download esp basic source from here

3 https://github.com/esp8266/Basic/tree/NewWebSockets

old https://www.esp8266basic.com/download.html


insert folders from folder Basic-NewWebSockets\Basic-NewWebSockets\libraries
to 
C:\Users\costycnc\Documents\Arduino\libraries 
(when install arduino is create automatically a folder Arduino\libraries  in C:\Users\costycnc\Documents

remove websockets folder because he was giving a error when compile

select Arduino -> Tools -> Board -> esp8266 board
open Arduino -> File -> Open -> Basic-NewWebSockets\ESP8266Basic\ESP8266Basic.ino

will be load all file automate from folder

compile 
