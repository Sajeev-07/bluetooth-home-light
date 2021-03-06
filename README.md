<!-----
NEW: Check the "Suppress top comment" option to remove this info from the output.

Conversion time: 9.566 seconds.


Using this HTML file:

1. Paste this output into your source file.
2. See the notes and action items below regarding this conversion run.
3. Check the rendered output (headings, lists, code blocks, tables) for proper
   formatting and use a linkchecker before you publish this page.

Conversion notes:

* Docs to Markdown version 1.0β30
* Fri Jul 30 2021 00:10:47 GMT-0700 (PDT)
* Source doc: Bluetooth Controlled 240V Bulb
* This is a partial selection. Check to make sure intra-doc links work.

WARNING:
Inline drawings not supported: look for ">>>>>  gd2md-html alert:  inline drawings..." in output.

* This document has images: check for >>>>>  gd2md-html alert:  inline image link in generated source and store images to your server. NOTE: Images in exported zip file from Google Docs may not appear in  the same order as they do in your doc. Please check the images!

----->

<h1><strong>Bluetooth Controlled home light (Bulb)</strong></h1>

<p>
Hello…

Nowadays Most of the equipment which is used in our life is being controlled by our smartphones. So we can make our work easy and we can use this things in many ways. This project is all about building the most simplified home automation device using an arduino and a bluetooth module. This one is very easy to build and it can be built in a few hours. In my version which I'm explaining right here, I can control home appliances using my Android smartphone. Let's have a look at the list of materials and tools you'll need.
</p>

<img src="https://github.com/Sajeev-07/bluetooth-home-light/blob/main/SOURCE/IMAGES/final.jpg?raw=true" width="255.68"  height="202.56" alt="alt_text" title="image_tooltip">



<img src="https://github.com/Sajeev-07/bluetooth-home-light/blob/main/SOURCE/IMAGES/final1.jpg?raw=true" width="255.68"  height="202.56" alt="alt_text" title="image_tooltip">

</p>

<p><strong>Author</strong></p>

<p>
Sajeev Punithakaran
</p>

<p><strong>Acknowledgment</strong></p>

<ul>
      <li>Aravith Panch , Co-founder and Director of Innovation, DreamSpace Academy , Batticaloa , Sri Lanka.</li>
      <li>Kishoh Navaretnarjah , Co-founder and Director, DreamSpace Academy.</li>
</ul>

<p>
<strong>Step 1 : Collecting components</strong>
</p>
<p>


<img src="https://github.com/Sajeev-07/bluetooth-home-light/blob/main/SOURCE/IMAGES/compenents.jpg?raw=true" width=" 424.32" height="290.88" alt="alt_text" title="image_tooltip">



<img src="https://github.com/Sajeev-07/bluetooth-home-light/blob/main/SOURCE/IMAGES/Bluetooth%20Controlled%20240V%20Bulb%20(1).jpg?raw=true" width="188.16" height="290.88" alt="drawing">

</p>
<p>
Here we’re going to make a bluetooth control  240V Bulb by using an Arduino UNO.So let's collect the required components as I mentioned above before building the Circuit.
</p>
<p>
<strong>The components are :</strong>
</p>


<ol>

<li>Arduino UNO	 - 1

<li>HC-06 Bluetooth module - 1

<li>LED  - 1

<li>Relay Module - 1 

<li>Line Board - 1

<li>Bulb (240V) - 1

<li>Bulb Holder, Wire and 2 Pin Plug

<li>Short female header as we required

<li>Short male header as we required

<li>Jumper wires as we required
</li>
</ol>
<p>
After collecting the components, let's start to implement it on a breadboard.
</p>
<p>
<strong>Bluetooth Module, HC-06</strong>
</p>
<p>

                


<img style = "justified" src="https://github.com/Sajeev-07/bluetooth-home-light/blob/main/SOURCE/IMAGES/bluetooth%20module.png?raw=true" width="" alt="alt_text" title="image_tooltip">

</p>
<p>
The HC-05 Bluetooth module is one of the most popular and inexpensive modules used for RF communications and it is easy to implement in your projects. The module has a range of 10 meters, and can be easily set using AT commands and can be programmed both as master and a slave. The module allows to transform a UART \ USART port more commonly known as serial into a Bluetooth port, generally with SPP (Serial Port Profile) profile, thus becoming a serial over Bluetooth. Normally this device is used when you want to communicate with a microcontroller like Arduino with the outside world, where the outside world can be a SmartPhone, a Personal Computer, or other device equipped with a Bluetooth connection.
</p>
<h2>Working principle of Arduino-Bluetooth Module</h2>


<p>
In this project, there are four main components used: Android smartphone Bluetooth application, Bluetooth transceiver, Arduino device, and 1 Channel Relay 
</p>
<p>
Module.
</p>
<p>




<img src="https://github.com/Sajeev-07/bluetooth-home-light/blob/main/SOURCE/IMAGES/diagram.jpg?raw=true" width="637.44" height="107.52" alt="drawing">

</p>
<p>
The Android app sends the serial data to the connected Bluetooth Module HC-06 by clicking ON button. The Bluetooth device receives the data from the app and sends it through the TX pin of the Bluetooth module to the RX pin of Arduino. The Arduino device reads the input data and processes it according to the program uploaded inside it and generates the output to 1 Channel Relay Module.
</p>
<p>
When the Bluetooth application's button turns ON, it sets the home light ON, and when the Bluetooth application's button turns OFF, it sets the home light OFF.
</p>
<p>
<strong>Step 2 : Interfacing HC-05 Bluetooth Module.</strong>
</p>
<p>




<img src="https://github.com/Sajeev-07/bluetooth-home-light/blob/main/SOURCE/IMAGES/blutooth-connect2.jpg?raw=true" width="298.56" height="218.88" alt="alt_text" title="image_tooltip">





<img src="https://github.com/Sajeev-07/bluetooth-home-light/blob/main/SOURCE/IMAGES/blutooth-connect.jpg?raw=true" width="298.56" height="218.88" alt="alt_text" title="image_tooltip">

</p>
<p>
The HC-05 Bluetooth module has generally four pins:
</p>
<ul>

<li>TX pin - Transmitting pin is used to transmit the signal to the receiver.

<li>RX pin - The pin that receives the signal from the transmitter.

<li>VCC pin - The power supply pin (+)

<li>GND pin - The power supply pin (-)
</li>
</ul>
<p>
The connection or interfacing of the module is as follows:
</p>
<ul>

<li>TX pin to the digital pin 0 (RX pin of arduino)

<li>RX pin to the digital pin 1 (TX pin of arduino)

<li>VCC pin to the Positive railings of the breadboard

<li>GND pin to the negative railings of the breadboard
</li>
</ul>
<p>
<strong>Step 3 : Interfacing Relay module </strong>
</p>
<p>

            

<img src="https://github.com/Sajeev-07/bluetooth-home-light/blob/main/SOURCE/IMAGES/relay.jpg?raw=true" width="288" height="136.32" alt="alt_text" title="image_tooltip">

</p>
<p>
The relay is an electromechanical device consisting of a winding and one or more mechanical contacts, it is used for interrupting and switching AC circuits using very low DC voltage. Which means we can control Electrical appliances in our house using Arduino or any other Microcontroller.
</p>
<p>
Here we’re going to use a relay module which is an electrically operated switch that can be turned on or off, letting the current go through or not, and can be controlled with low voltages, like the 5V provided by the Arduino pins 
</p>
<p>
Controlling a relay module with the Arduino is as simple as controlling any other output as we’ll see later on.This relay module has one channel (the blue cube). There are other models with two, four and eight channels. This module should be powered with 5V, which is appropriate to use with an Arduino.
</p>
<p>
This module should be powered with 5V, which is appropriate to use with an Arduino.and here we’re going to use this relay to control 240V bulb via bluetooth with arduino. 
</p>
<p>
Relay Pinouts :
</p>
<p>
The following figure shows the relay module pinout.
</p>
<p>
             



<img src="https://github.com/Sajeev-07/bluetooth-home-light/blob/main/SOURCE/IMAGES/relay-pinouts.jpg?raw=true" width="260.16" height="187.2" alt="alt_text" title="image_tooltip">

</p>
<p>
The 3 pins on the left side of the relay module(blue cubes) connect high voltage, and the pins on the right side connect the component that requires low voltage-- the Arduino pins.
</p>
<p>
The high-voltage side has two connectors, each with three sockets: common(COM), normally closed(NC). And normally open (NO).
</p>
<p>
<strong>Main voltage connections :</strong>
</p>
<p>





<img src="https://github.com/Sajeev-07/bluetooth-home-light/blob/main/SOURCE/IMAGES/normally-open.jpg?raw=true" width="260.16" height="187.2" alt="alt_text" title="image_tooltip">



<img src="https://github.com/Sajeev-07/bluetooth-home-light/blob/main/SOURCE/IMAGES/normally-close.jpg?raw=true" width="265.16" height="187.2" alt="alt_text" title="image_tooltip">

</p>
<p>
The high-voltage side has two connectors, each with three sockets: common (COM), normally closed (NC), and normally open (NO).
</p>
<ul>

<li><strong>COM :</strong> Common pin

<li><strong>NC (Normally closed) : </strong>the normally closed configuration is used when you want the relay to be closed by default.meaning the current is flowing unless you send a signal from the Arduino to the relay module to open the circuit and stop the current.

<li><strong>NO (Normally open) : </strong>the normally open configuration works the other way around: The relay is always open , the circuit is broken unless you send a signal from the arduino to close the circuit.
<p>

    If you just want to light up a lamp occasionally, it is better to use a normally-open circuit configuration.
</p>
</li>
</ul>
<p>
<strong>Pin wiring :</strong>
</p>
<p>
The low-voltage side has a set of four pins and a set of three pins.
</p>
<p>



<img src="https://github.com/Sajeev-07/bluetooth-home-light/blob/main/SOURCE/IMAGES/relay-pin.png?raw=true" width="368.64" height="192.96" alt="alt_text" title="image_tooltip">

</p>
<p>
The set at the right consists of <strong>VCC</strong> and <strong>GND</strong> to power up the module, and input 1 (<strong>IN1</strong>) and input 2 (<strong>IN2</strong>) to control the bottom and top relays, respectively.
</p>
<p>
The second set of pins consists of <strong>GND</strong>, <strong>VCC</strong>, and<strong> JD-VCC</strong> pins. The JD-VCC pin powers the electromagnet of the relay.
</p>
<ul>

<li><strong>COM :</strong> Common pin

<li><strong>In :  </strong>controls the first relay (it will be connected to an Arduino digital pin)

<li><strong>VCC : </strong>Goes to 5V pin of Arduino
</li>
</ul>
<p>
<strong>Connection between Relay Module, Bulb, and input power:</strong>
</p>
<ol>

<li>Connect common-point (<strong>com</strong>) of the Relay Module with home light.

<li>Connect normally-open (<strong>no</strong>) of the Relay Module with power.

<li>Connect the remaining one home light wire with the <strong>power source</strong>.
</li>
</ol>
<p>
<strong>Write an Arduino program to control the home light using Bluetooth Module,1 Channel Relay Module with Android application</strong>
</p>
<p>
Compile and upload your code into the Arduino device using Arduino USB cable. While uploading the code try  to disconnect other components from Arduino.
</p>


```

char Incoming_value = 0;

void setup() {
  Serial.begin(9600);

  pinMode(13, OUTPUT);

  }

    void loop() {

    if(Serial.available() > 0)

    {

      Incoming_value = Serial.read();

      Serial.print(Incoming_value);

      Serial.print("\n");

      if (Incoming_value == 'a')

        digitalWrite(13, HIGH);

      else if (Incoming_value == 'b')

         digitalWrite(13, LOW);
      }

}
```

<p>
<strong>Home Automation App : </strong>
</p>
<p>
You need an app (<a href="https://play.google.com/store/apps/details?id=com.darkbrothers.automation&hl=en_IN">download here</a>) to control the Home appliances using Bluetooth. After downloading follow these steps to add a Room and components.
</p>
<p>
<strong>Step 1</strong> <strong>:</strong> Open Bluetooth settings of mobile and pair the HC-05 Module. Kindly note that only paired devices will appear in the Android App.
</p>
<p>
<strong>Step 2 :</strong> Open the app and click on the Bluetooth icon to connect with the Bluetooth device.
</p>
<p>
<strong>Step 3 :</strong> Click on + icon at the bottom right of screen to Add a Room. If Bluetooth is being Connected the Bluetooth icon will turn blue in color.
</p>
<p>
<strong>Step 4 :</strong> Here you can change Room name, picture and add new devices. Click + to add a new device and swipe right to delete.
</p>
<p>
<strong>Step 5 : </strong>After saving you can send data to the connected Bluetooth Device. Make sure to Pair your Bluetooth device before using the App
</p>
<p>
<strong>     </strong>


<img src="https://github.com/Sajeev-07/bluetooth-home-light/blob/main/SOURCE/IMAGES/app01.png?raw=true" width="181.56" height= "234.04" alt="alt_text" title="image_tooltip">



<img src="https://github.com/Sajeev-07/bluetooth-home-light/blob/main/SOURCE/IMAGES/app02.png?raw=true"  width="181.56" height= "234.04" alt="alt_text" title="image_tooltip">



<img src="https://github.com/Sajeev-07/bluetooth-home-light/blob/main/SOURCE/IMAGES/app03.png?raw=true"  width="181.56" height= "234.04" alt="alt_text" title="image_tooltip">

</p>
<p>


<img src="https://github.com/Sajeev-07/bluetooth-home-light/blob/main/SOURCE/IMAGES/app04.png?raw=true" width="181.56" height= "234.04" alt="alt_text" title="image_tooltip">



<img src="https://github.com/Sajeev-07/bluetooth-home-light/blob/main/SOURCE/IMAGES/app05.png?raw=true"  width="181.56" height= "234.04" alt="alt_text" title="image_tooltip">

</p>
<p>
<strong>Connection : </strong>
</p>

<img src="https://github.com/Sajeev-07/bluetooth-home-light/blob/main/SOURCE/IMAGES/circuit.jpg?raw=true"  idth="640.32" height="486.72" alt="alt_text" title="image_tooltip">

<p>
<strong>If it works on the breadboard, let's make the project on a line board with the same components.</strong>
</p>
<p>
Here we are going to use a line board instead of the breadboard.we have to solder all of the components as we require with the help of the diagram above.
</p>
<p>




<img src="https://github.com/Sajeev-07/bluetooth-home-light/blob/main/SOURCE/IMAGES/pcb1.jpg?raw=true" width="104.64" height="104.64" alt="alt_text" title="image_tooltip">



<img src="https://github.com/Sajeev-07/bluetooth-home-light/blob/main/SOURCE/IMAGES/pcb2.jpg?raw=true" width="104.64" height="104.64" alt="alt_text" title="image_tooltip">



<img src="https://github.com/Sajeev-07/bluetooth-home-light/blob/main/SOURCE/IMAGES/pcb3.jpg?raw=true" width="104.64" height="104.64" alt="alt_text" title="image_tooltip">


<img src="https://github.com/Sajeev-07/bluetooth-home-light/blob/main/SOURCE/IMAGES/pcb4.jpg?raw=true" width="104.64" height="104.64" alt="alt_text" title="image_tooltip">



<img src="https://github.com/Sajeev-07/bluetooth-home-light/blob/main/SOURCE/IMAGES/pcb5.jpg?raw=true" width="104.64" height="104.64" alt="alt_text" title="image_tooltip">

</p>

<p>
<strong>Thank you...</strong>
</p>