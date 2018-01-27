# Arduino-Dimmer

This project should guide you through the basics of setting up a circuit and controlling it with an Arduino. We'll cover topics such as ohm's law, voltage, current, and resistance, but more advanced topics will be left to another time and the reader's own discretion.

# Instructions

## It's alive

Take your Arduino and plug it into your laptop using a full sized USB cable. You should see the on led light up like this:

![Arduno Unio](https://lh3.googleusercontent.com/sUvDeIEGpGDZUC-w0v8qsllp8dG3f3zM03DdYGp4HzV9fAIGj8K00A33d6ti9Txl3hHpJ_zOwbrO20k-FJWtc4uDJmoPIRHABN4sbRhli86f3svsEBgfkSvQhO5yEA7RlieZnC_bm_GrlwzwdgGaaJT7kOjHnMuIgV5TXXSwSHmgAYosPE992H23Ez9NEupBZCi3J6Po5kIQ7GJPnW0iJx1YgPNZf6kI6lEMCTZi8CCLxUaDwY7gX4TcUji3R6hKGBeteUzjLQlyY6qspCg1kh9HthxZndsySTcuZjEqOB5AgVgWAmG9FI7iNwTiq9tDdBoqZ-Wr3e4QpZpUrdo8t6gJYv-vdA4eG13hpFre3-0zetF6UrBHEmBV5Zq7MTMOwqCTJ8bvGeQYBLd2GkPnjGI29zEUn7BXM9zjw4geKlnGzxAPN-nczYwEK8xXPQRJqZ-_ALG_MjI0IzskqOdOIJcxBl0IMGPvr9PVsLIa-UXszgZ9xSCZr5QMVQeWb7l37vNz6Tu7Nmpzou8nDrIicKyAN3lSCCfwPo-l5f705Etj1kYig5JsSW2CQKjJtMkLSSn5FQ=w1247-h935-no)

This means your Arduino has power and can be programmed via the IDE, we'll get back to that.

## Let there be light

Take out the breadboard and note how it's set up. At the top and bottom are two rows of holes labeled with a - and a +, these are meant for the positive and negative sides of the circuit and all the holes along these rows are hooked up under the plastic case. Similarly there are a group of columns labeled 1 through 30 and rows labeled a through e directly under these. This is a where most of this project will be constructed. Here each column is connected under the plastic. This lets us connected wires together without using trying to physically hold the wires together.

Let’s take a break to explain how electricity works in a circuit. People like to think of an electric circuit like water in a pipe. The water in this analogy flows from the positive side of the circuit to the negative side of the circuit. When the water is flowing there are two important variables to think about. How hard the water is pushing, the pressure, and how much is flowing through the pipe. There are two similar variables in a circuit. Voltage basically describes how much pressure is behind the electrons and current describes how many electrons are flowing through a wire. Most electronics works by keeping the voltage constant and letting the current vary as applications draw more and less current. Just like a pipe the current going through it can be restricted. We call the devices that do this resisters and they obey ohm's law. The total current in a circuit will equal the total voltage divided by the total resistance or I = V/R. The reason this is important is that we'll be using a device called an LED which can only take relatively low levels of current so we have to restrict the amount of current with a resistor. We have two resistors to choose from, but we'll be using the one without a red band.

LED stands for light emitting diode. The first two words make sense. It emits light, but diode may not be familiar to you. It refers to an LED's electronic characteristic. It's special because like all diodes it will only let electricity through in one direction. On an LED the positive end is marked by being longer.

1. So to make our circuit we will hook up the a wire from the 5V pin to our breadboard.
2. Now we need to hook up the negative side of the circuit. 3. We’ll hook up the ground pin to the - row on the top.
4. Let’s add the resistor. Connect the resistor between the - row and a column, let’s do the one right next to the positive lead.
5. Finally let’s put the LED in and watch it light up. Make sure to put the longer end in the positive column.

![LedWiring](https://github.com/hacksu/Arduino-Dimmer/blob/master/imgs/Screenshot-2018-1-26%20Autodesk%20Circuits(1).png?raw=true)

## Controlling the Brightness

### Wire up the button
![ButtonWiring](https://github.com/hacksu/Arduino-Dimmer/blob/master/imgs/Screenshot-2018-1-26%20Autodesk%20Circuits.png?raw=true)

### Install the Arduino IDE
[Arduino IDE Download](https://www.arduino.cc/en/Main/Software)

### Writing the Code
``` cpp
bool last = LOW;
int light = 0;

void setup() {
    // set up pin inputs
    pinMode(12, INPUT);
    pinMode(11, OUTPUT);
}

void loop() {
    bool current = digitalRead(12);
    if (current != last) {
        light += 16;
    }
    analogWrite(11, light);
    last = current;
}
```

### Select your Board
![BoardType](https://github.com/hacksu/Arduino-Dimmer/blob/master/imgs/Screenshot_20180126_191816.png?raw=true)

### Select the Port
![Port](https://github.com/hacksu/Arduino-Dimmer/blob/master/imgs/Screenshot_20180126_192002(1).png?raw=true)

### Run 
![RunButton](https://github.com/hacksu/Arduino-Dimmer/blob/master/imgs/Screenshot_20180126_192952(3).png?raw=true)