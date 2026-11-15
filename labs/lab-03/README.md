# Lab 3 – THINK + ACT: Sense → Process → Act

- Team name:
- Prototype or display label:
- Members' GitHub usernames:
- Shared Wokwi project link:

## 1. Explain the program and connections

In one sentence, describe what happened to the startup and loop messages when you ran and restarted the Activity 2 program.

Use one or two sentences for each explanation. Include a labelled sensor → controller → actuator chain; text is sufficient. Include the LCD as an additional output.

- Why must the sensor, servo and Nano share GND?
- Why does AO connect to an analogue input, and what would change in the code if you used A1 instead of A0?
- What does D9 carry, which wires supply the servo's power, and what would change if the signal moved to D8?

## 2. Observe the sensor

Record two live input conditions before implementing the decision. The light setting is in lux; the sensor reading is the whole number returned by `analogRead(A0)`, from 0 to 1023.

| Condition | Simulated light setting (lux) | Observed sensor reading (0–1023) |
| --- | --- | --- |
| Less light | | |
| More light | | |

Explain how the reading changes with light. Why does the 10-bit ADC return 0–1023 even though the Nano stores the result in a 16-bit `int`?

## 3. State the requirement

- Threshold T (sensor reading):
- Closed command (degrees):
- Open command (degrees):

State the rule, including what happens at equality, and justify the threshold using your observations. Keep T between 1 and 1022.

## 4. Test and revise

Write predictions before running the tests. Record actual results separately and state whether each agrees. Mark an unexecuted test as “Not run.”

| Test | Input value and source | Expected command and response | Observed command, virtual response and LCD state | Agreement or correction |
| --- | --- | --- | --- | --- |
| Below threshold | T − 1; injected software input | | | |
| At threshold | T; injected software input | | | |
| Above threshold | T + 1; injected software input | | | |
| Bright live input | Record the light setting and observed count. | | | |
| Live recovery | Record the light setting and observed count. | | | |

Explain one correction or limitation. Distinguish the injected tests from tests using the simulated sensor.

In the two live-test rows, record whether the LCD reading and command agree with the serial output and servo response.

Insert **one screenshot** showing the complete circuit, readable LCD and serial output during a live test. Use your actual filename, for example `![Circuit and live test](controller.png)`, and add a caption identifying the condition and response. The LCD must show your team or prototype label, current reading and commanded state. The other results belong in the table; additional screenshots are not required.

## 5. Connect to the final project

In two or three sentences, describe one useful project input → decision → output chain. Identify the sensor signal and actuator interface, and one physical check still needed. Where relevant, relate sensor placement or moving-part clearance to your Lab 2 design.

## Source files

- [Controller program](sketch.ino).
- [Circuit diagram](diagram.json).
- [Library list](libraries.txt).

Restore `int reading = analogRead(A0);` in the final program so it uses the sensor rather than a fixed test value. Check that all three files are present beside this report and that the links open. Include both Servo and LiquidCrystal I2C in the library list. Save the same final version in Wokwi, then ask another member to open the shared project link above and run it. The GitHub SHA identifies the assessed version; the Wokwi link provides a runnable copy.

## Contributions

Use one row per member. Each member should commit meaningful work using their own GitHub account and explain their practice or team contribution. Prediction, coding, testing, interpretation, paired work and documentation all count when supported by evidence.

| GitHub username | Contribution and related evidence | One result or concept I can explain |
| --- | --- | --- |
| | | |

## Sources and AI use

Credit sources beyond the supplied course checkpoints. If AI was used, identify the tool, relevant prompt and output, and your verification or corrections. Otherwise, write “No AI used.”

Before submission, check this record against the handout supplied for Lab 3. Submit your team name, ordinary repository URL, report path, latest full `main` SHA and shared Wokwi project link in Canvas after all files are saved. Keep the SHA out of this report.
