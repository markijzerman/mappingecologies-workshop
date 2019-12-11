# Mapping Ecologies sensor document: Water and air quality

## DFrobot Turbidity sensor
Detecs water quality, uses light to detect suspended particles.
Turbidity is measured in NTU (mg/L)

Link: https://wiki.dfrobot.com/Turbidity_sensor_SKU__SEN0189

Arduino code:

```void setup() {
  Serial.begin(9600); //Baud rate: 9600
}
void loop() {
  int sensorValue = analogRead(A0);// read the input on analog pin 0:
  float voltage = sensorValue * (5.0 / 1024.0); // Convert the analog reading (which goes from 0 - 1023) to a voltage (0 - 5V):
  Serial.println(voltage); // print out the value you read:
  delay(500);
}
```


## MQ-135 Air Quality sensor
Detects PPM (Particles Per Million) in real time.
See under "What is PPM?": https://www.instructables.com/id/Air-Qualiy-Monitoring/

https://create.arduino.cc/projecthub/karimmufte/arduino-and-mq-135-gas-sensor-with-arduino-code-a8c1c6

In my studio, ~43PPM?

Arduino code:

```int sensorValue;

void setup(){
Serial.begin(9600);                            // sets the serial port to 9600
 }
void loop(){sensorValue = analogRead(0);       // read analog input pin 0
Serial.print("AirQua=");
Serial.print(sensorValue, DEC);               // prints the value read
Serial.println(" PPM");

delay(100);                                   // wait 100ms for next reading
}
```


# How to get in sensor data on Max or Touchdesigner?
Touchdesigner tutorial: https://www.youtube.com/watch?v=bUVavS6tNPc
Max will be done live in the workshop
 
# Recording Touchdesigner data
See example .toe file in this directory