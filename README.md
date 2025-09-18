# Smart-Pet-Feeder
The Smart Pet Feeder automatically dispenses food for your pet on command. It monitors food levels in the storage container and feeding bowl with ultrasonic sensors and updates the Blynk app in real time. Owners can remotely control the servo-driven dispenser and receive alerts when the food supply is low or the bowl is empty.


Configurationn details
Component	                              Pin on Component	               ESP8266 (NodeMCU) GPIO           	Notes
Ultrasonic Sensor 1 (HC-SR04)	               VCC	                              5 V	                        Power
	                                           GND	                              GND	                        Ground
	                                           Trig                             	GPIO4 (D2)	                Trigger pin
	                                           Echo                             	GPIO5 (D1)	                Echo pin
Ultrasonic Sensor 2 (HC-SR04)              	VCC	                                5 V	                        Power
                                          	GND	                                GND	                        Ground
	                                          Trig                              	GPIO0 (D3)                	Trigger pin
                                          	Echo	                              GPIO2 (D4)	                Echo pin
Servo Motor	                                VCC (Red)	                          5 V	                        Power
	                                          GND (Brown/Black)                 	GND	                        Ground
	                                          Signal (Orange/Yellow)	            GPIO13 (D7)	                PWM control
Power                                       	—	                                5 V & GND rails	            Supplied via Arduino Uno USB or external 5 V source
