# IR Object Detector – LED Starts On (Infrared)

Video: https://www.youtube.com/watch?v=1du7LRB1-hc

---

![IR_Object_Detector_LED_Starts_On_(Infrared)](textures/IR_Object_Detector_LED_Starts_On_(Infrared).webp)

---

This circuit demonstrates how to use **infrared light** to detect when an object passes between two points. The circuit begins with the LED **on by default**, and when the IR beam is interrupted, the LED turns **off**.

This “normally on” behavior makes the circuit easy to test, reliable, and useful for practical applications such as cat traps for rescues, counters, and object detection systems.

---

## Components Used

* **Power Supply:** 2 × D batteries (3 volts total)
* **Resistors:**

  * 220 Ω (limits current through the IR emitter)
  * 150 Ω (limits current through the LED)
* **IR Emitter:** an LED that emits **infrared light**
* **IR Receiver:** a **phototransistor** in a clear LED-style package that reacts to infrared light
* **Transistor:** BC547 (NPN bipolar junction transistor)
* **Indicator LED:** green LED (shows detection status)
* **Breadboard and jumper wires**

---

## How the Circuit Works

### 1. Power Distribution

Two D-cell batteries supply **3 volts**. The red wire connects the positive rail, and the green wire connects the negative rail. Jumpers connect the top and bottom rails so that the breadboard has a single positive line and a single negative line.

---

### 2. The IR Emitter (Infrared LED)

* The IR emitter looks like a small clear LED but produces invisible infrared light.
* A **220 Ω resistor** is connected in series with it.

  * **Why?** The resistor prevents too much current from flowing through the IR LED, protecting it from damage.
* When powered, the emitter continuously sends out a beam of infrared light.

---

### 3. The IR Receiver (Phototransistor)

* The IR receiver also looks like a small LED, but it is actually a **phototransistor**.
* When the infrared beam from the emitter reaches it, it allows a small current to flow.
* When the beam is blocked by an object, the phototransistor stops conducting.

---

### 4. The BC547 Transistor

* The **BC547 NPN transistor** acts as a **switch and amplifier**.
* The small current from the IR receiver is connected to the **base** of the BC547.
* When IR light is detected, the phototransistor allows current into the base, switching the BC547 “on.”
* This allows a stronger current to flow from **collector to emitter**, powering the green LED.

---

### 5. The Green LED (Indicator)

* The green LED shows the circuit’s detection status.
* It is connected with a **150 Ω resistor** to limit current and prevent burnout.
* When the IR beam is uninterrupted:

  * Phototransistor conducts → BC547 switches on → LED **glows**
* When the IR beam is blocked:

  * Phototransistor stops conducting → BC547 switches off → LED **turns off**

---

## Behavior Explained

* **LED normally ON:** This shows that the emitter, receiver, and transistor are working correctly.
* **LED turns OFF when beam blocked:** This indicates an object has entered the detection zone.
* **Why this is useful:**

  * Easier to test—if the LED is off by mistake, you instantly know something is wrong.
  * Safer for real-world use cases like traps or counters, since the “on by default” state ensures power and connections are working.

---

## Key Learning Points for Beginners

1. **Resistors are protective devices.**

   * 220 Ω protects the IR emitter.
   * 150 Ω protects the green LED.

2. **Diodes and LEDs only allow current in one direction.**

   * Both the emitter and LED have polarity: long leg is positive, short leg with flat edge is negative.

3. **Phototransistors are light-controlled switches.**

   * Instead of a base wire, light controls the current flow.

4. **Transistors amplify signals.**

   * A tiny current at the base controls a larger current between collector and emitter.

---

## Applications

* **Cat traps or humane animal traps:** A piece of paper or plastic can block the beam until disturbed by the animal, signaling its presence.
* **People counters:** Mounted across a doorway, the circuit counts how many times the beam is interrupted.
* **Obstacle detection:** Robots can use it to sense nearby objects.
* **Security systems:** Acts as a tripwire for alarms.

---

## Closing Notes

This circuit introduces several foundational electronics concepts:

* Current limiting with resistors
* Infrared light transmission and detection
* Using a transistor as a switch and amplifier
* Basic logic behavior (normally high → active-low when triggered)

It is simple enough for beginners yet illustrates principles that engineers continue to use in more advanced systems.

---


//----//

// Dedicated to God the Father  
// All Rights Reserved Christopher Andrew Topalian Copyright 2000-2025  
// https://github.com/ChristopherTopalian  
// https://github.com/ChristopherAndrewTopalian  
// https://sites.google.com/view/CollegeOfScripting

