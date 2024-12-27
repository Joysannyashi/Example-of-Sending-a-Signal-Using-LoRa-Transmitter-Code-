//Example-of-Sending-a-Signal-Using-LoRa-Transmitter-Code-
#include <SPI.h>
#include <LoRa.h>

void setup() {
  Serial.begin(9600);
  LoRa.begin(915E6);  // Initialize LoRa on 915 MHz
}

void loop() {
  LoRa.beginPacket();
  LoRa.print("Hello LoRa");
  LoRa.endPacket();
  
  delay(1000);  // Send message every second
}
