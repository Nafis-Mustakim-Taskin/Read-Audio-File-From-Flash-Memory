#include <SPIMemory.h>
SPIFlash flash(10);
uint32_t _address= 0;
uint8_t dataIn;
void setup() {
flash.begin();
flash.setClock(1800000);
Serial.begin(2000000);
pinMode(A0,OUTPUT);
pinMode(9,INPUT);
pinMode(10,INPUT);
int in;
//digitalWrite(6, LOW);
uint32_t maxPage = flash.getMaxPage();
uint32_t manID = flash.getManID(); // Function is used to get the manufacturer
uint32_t cap = flash.getCapacity(); // Function is used to get the unique ID
//int Output = "";
Serial.print(F("Chip Manufacturer ID: 0x"));
Serial.println(manID, HEX);
Serial.print(F("Capacity: "));
Serial.println(cap); // The unique ID is printed as a decimal number
Serial.print(F("Maximum pages: "));
Serial.println(maxPage);
//noTone(8);
}
void loop() {

  {
for(_address =100;_address<118656;_address++)
  {
  dataIn = flash.readByte(_address);
  Serial.println(dataIn);
  analogWrite(A0, dataIn);
  }
}
}
