# 2x4 Macropad

A small and cheap 8 key macropad.

## Parts Required
+ PCB
+ Arduino Pro Micro
+ 8 Cherry MX Compatible switches
+ 8 Keycaps

## Where to buy
If you can't or don't want to produce this PCB yourself, you can PM me on [Reddit](https://www.reddit.com/user/amtra5), and I can send you one for $2 + Shipping! (from Australia)

## Firmware
The official firmware is not quite ready yet! Until then, use the following guide to help you build your own.

### Pinout
The pinout for each of the buttons is as follows.
![](http://i.imgur.com/2kyTrjG.jpg)

### Example Arduino Code
```C
bool getState(pin) {
  // INPUT_PULLUP means that the pin is LOW when pressed and HIGH when released
  return (digitalRead(2) == LOW);
}

void setup() {
  // Initialise the first button
  // The pin for the first button corrosponds to 2
  pinMode(2, INPUT_PULLUP); 
}

void loop() {
  // Read the state of the button
  bool state = getState(2);
}
```
