# Target_Case_Study

## Problem discription:
In a language of your choice, write a program which will tell you how long it is until
the next bus on “BUS ROUTE” leaving from “BUS STOP NAME” going “DIRECTION”
using the api defined at http://svc.metrotransit.org/

“BUS ROUTE” will be a substring of the bus route name which is only in one bus
route

“BUS STOP NAME” will be a substring of the bus stop name which is only in one bus
stop on that route

“DIRECTION” will be “north” “east” “west” or “south”

Eg, if you wanted to know the next bus leaving from our Brooklyn Park campus to
our downtown campus:

$ go run nextbus.go “Express - Target - Hwy 252 and 73rd Av P&R - Mpls” “Target
North Campus Building F” “south”
2 Minutes
(note that that won’t return anything if the last bus for the day has already left)

Or if you wanted to take the light rail from downtown to the Mall of America or the
Airport:

$ nextbus.py “METRO Blue Line” “Target Field Station Platform 1” “south”
8 Minutes

## Build Process
use $javac NextBus.java to compile the program

then use $java NextBus "BUS ROUTE" "BUS STOP NAME" "DIRECTION"

I used IntelliJ IDE to write, compile, and run the program. If IntelliJ is to be used GSON must be configured in the project settings as a global library by adding the .jar

An example that seemingly works everytime is: "METRO Blue Line" "Mall of America Station" "north"
This should return either nothing because the light rail is at the station or an example of its output would 6 minutes

## Libraries:
the libraries/imports used are as follows:

  import com.google.gson.*;

  import java.io.*;
  
  import java.net.HttpURLConnection;
  
  import java.net.URL;
  
  import java.util.Date;
  
  
## Gson details  
(gson is a Java library made by Google that converts java objects into JSON representation)

Gson Download(s):
https://mvnrepository.com/artifact/com.google.code.gson/gson/2.8.5

Gson API: Javadocs for the current Gson release http://www.javadoc.io/doc/com.google.code.gson/gson
