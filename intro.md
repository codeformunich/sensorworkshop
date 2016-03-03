# Introductory Notes
## Sensors and the Internet of Things (IoT)
This workshop is about sensing things about the environment with electronic sensors and communicating this data to the outside world using the internet. The whole concept sometimes get's termed "Internet of Things" to signify that the internet is not just made up of computers but also items that are much closer to the natural environment, or your mouth (in the case of the networked fridge).

## Why now is the perfect time to start an IoT project?!
Quantifying the environment using electronics is nothing new. Probably many people can remember hobbyist electronics magazines with many fun projects to build out of simple components to detect wetness, noise, light and so on. The shelves of Conrad also abound with kits for building sensing projects of various kinds.

A few things have however shaken up the sensing scene in recent years. In particular programmable microcontrollers have allowed people to attach a sensor not just to some hardwired output but instead to a miniature computer chip which can be programmed to do different things depending on the sensor value or another sensor's value, or the day of the week, or, whatever. Building on the actual microcontroller chip have come easy-to-use platforms that standardise the programming language, programming method (getting the code that defines what you want the microcontroller to do to the microcontroller) and interfaces for input and output devices that can be attached. The most popular by far of these is the Arduino/Genuino platform (www.arduino.cc).

It's important to note that a basic Arduino (or other microcontroller platform) is fairly autonomous. It gets power, starts, and runs something. We attach it to a computer in order to upload a prepared program (often called "sketch") to the Arduino, and that's usually where the role of the computer ends. It is possible to send data back and forth between the computer and Arduino, and with some work this could provide us a way to send information to the internet, but this would defeat the purpose a little bit (why not just attach a sensor to the computer) and not make our sensing device very easy to deploy en mass! Fortunately, there have been many developments recently that have made internet communication from an Arduino both possible and straightforward for very little money. The most straightforward right now seems to be the "Pretzel Board IoT WiFi Board" of which we have three with us today. It is an Arduino-Nano compatible system which means we can use software that can interact with a Nano and consult references (i.e. what connections on the board do what) for the Nano in order to figure out how to connect sensors.

TODO: mention Raspberry?

## Sensor 101
Sensors fall into two basic categories: analog and digital. A simple digital sensor is a switch; it's either on or off and can be represented as 0 or 1. A temperature sensor might be analog, using a level of voltage to represent a temperature. The Pretzel board has analog and digital inputs.

It's also possible to communicate a scale of values on to a digital input. To do this, some kind of standard has to be used such as 1-Wire or I2C.

To make attaching sensors easier there are some systems which provide pluggable connections to mostly avoid needing to know what single connections ("pins") on the Arduino board are doing and what voltages are being used. One such system is Grove. Whether you want to use such a system or not, you still might end up having to use one or reverse-engineer it if the sensor you want is made by a provider of such a system. This is the case for the particulate matter sensor which we are using today from Grove. The other sensors are simpler and we need to be careful which pins we attach to which.


