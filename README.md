
# MAKERMANIA 2026

## Innovation Project Workbook

> Program Duration: 1 June 2026 – 4 July 2026
>
> Location: MBF Tinkerers' Lab 007
>
> Team Size: 3 Students
>
> Goal: Identify a real-world problem and develop an innovative, patentable, and implementable solution.

---

# 1. Team Identity

## 1.1 Team Name and Photo

### Draft Punk
<img width="1280" height="960" alt="Team_Draft_Punk" src="https://github.com/user-attachments/assets/67df0cfe-3f4b-4265-aa0b-5c207eee4154" />

## 1.2 Team Members

| Name | Role | Skills |
| ---- | ---- | ------ |
|   Ashish Waghmare   |  Team Lead   |   ML & Software integrator, Media Editor, Writer, Documentation     |
|  Aarush Srivatsava    |  Lead Ideator |   Electronics, Fusion, Hardware Integration    |
|   Shekhar Epili   |   Lead Hardware Design | Hardware Design , Soldering, Laser Cad    |

---

# 2. Problem Discovery

## 2.1 Observation Area

Where did you conduct your observations?
* Workshop (Electronics/Robotics Lab)

---

## 2.2 AEIOU Observation Sheet

### Activities

Q. What are users doing?

- Students borrowing components for practicals and projects, lab in-charge manually logging component usage, searching for missing or misplaced components.

### Environment

Q. What conditions affect them?

- College robotics/electronics lab with shared component storage, multiple students accessing the same rack, no formal tracking system in place.

### Interactions

Q. Who or what are they interacting with?

- Students interacting with the lab in-charge to request components, students using manual registers, lab in-charge managing returns and tracking usage.

### Objects

Q. What tools or products are used?

- Electronic components (ESP32, Arduino Nano, sensors, LoRa modules), manual registers, storage racks or boxes.

### Users

Q. Who are the primary users?

- Engineering students (primary), lab in-charge (secondary/admin).

---

## 2.3 Observation Log

| Observation | Evidence | Pain Point |
| ----------- | -------- | ---------- |
| Students forget to return components after use | Components found missing during next session | Component loss and replacement cost |
| Lab in-charge unaware of who took which component | No real-time tracking exists | Accountability gap |
| Components mixed or misplaced across storage | Time wasted searching before practicals | Inefficiency and lab disruption |

---

# 3. User Research

## 3.1 Interview Summary

Number of users interviewed: ______

## 3.2 Key Quotes

1. "Component leke bhaag jaate hai, rakhte nahi hai barabar."

2. "Itni college fee bharke bhi yehi milta hai."

3.

---

## 3.3 User Persona

## Persona 1

### Name
- Pranay Wani 

### Age
- 21

### Occupation
- Lab Head/Incharge

### Goals
- Wants more people contributing towards projects than taking care of components.

### Frustrations
- Students take components and don't return them properly, no reliable way to track inventory count.

### Needs
- A mapping system for inventory counting and component tracking.

##

## Persona 2

### Name
- Rajnarayan Hazra

### Age
- 20

### Occupation
- Student

### Goals
- Build a culture where people are confident enough to pick up hardware and electronics projects and get into a flow state of building.

### Frustrations
- No accountability or proper component management, causing multiple people to repeatedly handle the same logistics tasks manually instead of it being automated.

### Needs
- A system that handles inventory on its own and makes the entire component access process smooth and frictionless.

---

# 4. Problem Framing

## Problem Statement

- User (engineering student) needs a way to borrow and return lab components with accountability because components frequently go missing, lab in-charges have no real-time tracking, and manual registers are unreliable.

---

## How Might We Questions

1.How might we authenticate students quickly without adding friction to the component issuing process?

2.How might we automatically track whether a component has been returned on time?

3.How might we alert the lab in-charge before a component goes overdue?


---

## Opportunity Ranking

| Criteria         | Score |
| ---------------- | ----- |
| Severity         |       |
| Frequency        |       |
| Feasibility      |       |
| Novelty          |       |
| Market Potential |       |
| Total            |       |

---

# 5. Solution Ideation

## Brainstormed Ideas

| Idea | Advantages | Challenges |
| ---- | ---------- | ---------- |
| Manual register with strict rules | No cost | Still unreliable, human error |
| QR code-based digital log | Low cost, familiar | No physical access control |
| RFID-based smart rack with locking boxes |  Automated, accountable, real-time | Higher build cost and complexity |
 

---

## Selected Concept

- RFID-based smart rack

Q. Why was this concept chosen?

- The RFID-based smart rack was chosen because it combines authentication, physical access control, presence detection, and automated alerts in one system - replacing manual processes entirely while staying low-cost with ESP32.

---

# 6. System Design

## High-Level Description

Q. Explain your solution.

- A student scans their college RFID card, selects a component from the display menu, and the corresponding box unlocks via servo motor. An IR sensor detects component removal and starts a return timer. If the component isn't returned in time, the system triggers a buzzer, LED warning, and Wi-Fi-based alert to the lab in-charge.

---

## Block Diagram

Insert diagram here.

<img width="1448" height="1086" alt="image" src="https://github.com/user-attachments/assets/ec1c3927-d057-4ec5-9685-a98fbc891a81" />


---

## Inputs

Q. List sensors, user inputs, data sources.

-RFID card scan (student ID)
-Button/encoder input for component selection
-IR sensor / reed switch (component presence detection)

---

## Outputs

Q. List displays, actuators, software outputs.

- OLED/LCD display (menu, student name, status)
- Solenoid (box lock/unlock)
- LED indicators (status per box)
- Buzzer (alerts)
- Wi-Fi notification (overdue alert)

---

# 7. Technical Planning

## Electronics

| Component | Purpose |
| --------- | ------- |
| ESP32 | Main controller, Wi-Fi connectivity |
| RFID Reader (RC522) | Student authentication via college ID card |
| Solenoid | Lock/unlock individual component boxes |
| IR Sensors / Reed Switches | Detect component presence in each box |
| OLED / LCD Display | Show menu, student info, status |
| LEDs | Visual status indicators per box |
| Buzzer | Audible alert for overdue/system feedback |

---

## Software

| Tool | Purpose |
| ---- | ------- |
| Arduino IDE / PlatformIO | ESP32 firmware development |
| MFRC522 Library | Sending overdue notifications |
| SPIFFS / SD card | Local data storage for logs |

---

## Mechanical / CAD

Q. Describe fabricated components.

- Four enclosed storage boxes with solenoid-controlled locks. Each box has a slot for the IR sensor. The rack holds all four boxes in a fixed grid layout (A1-A4).


---

# 8. Prototype Development

## Version 1

Description:

Lessons Learned:

---

## Version 2

Description:

Lessons Learned:

---

## Final Prototype

Description:

---

# 9. Testing & Validation

## Testing Plan

| Test | Success Criteria |
| ---- | ---------------- |
|      |                  |
|      |                  |

---

## User Feedback

| User | Feedback | Action Taken |
| ---- | -------- | ------------ |
|      |          |              |

---

# 10. Innovation Assessment

## Existing Solutions

Q. List competing products.

**Existing Solutions**

- Manual lab registers
- Basic barcode/QR scanning systems
- Industrial smart cabinets (expensive, not student-accessible)



---

## What Makes This Different?

Uses a student's existing college RFID ID card - no new hardware needed on the user side. Combines physical access control, sensor-based detection, and automatic overdue alerts in a single low-cost ESP32 system designed specifically for college labs.

---

## Innovation Score

| Parameter       | Score |
| --------------- | ----- |
| Novelty         |       |
| Technical Depth |       |
| Feasibility     |       |
| Impact          |       |
| Scalability     |       |

---

# 11. Intellectual Property

## Prior Art Search

Patents / Products Found:

---

## Novel Features

1. RFID-authenticated physical box locking tied to a return timer

2. Sensor-based real-time component presence detection per box

3. Automated Wi-Fi overdue alert system for lab in-charge

---

## Provisional Patent Draft

### Title
- Smart Accountable Lab Component Rack with RFID Authentication and Automated Return Tracking

### Abstract
- An ESP32-based smart storage rack for electronics labs that uses RFID card authentication, servo-controlled box locking, presence detection sensors, and Wi-Fi alerts to automate the component issuing and return process.

### Problem
- Lab components are frequently lost or not returned because there is no automated accountability system - only manual registers that are slow and error-prone.

### Solution
- An RFID-authenticated rack with four smart boxes, each with servo locks and IR sensors, tracked by an ESP32 that logs issue/return times and sends overdue alerts over Wi-Fi.

### Claims

1. RFID-based student authentication linked to component access control
2. Per-box locking triggered only after authenticated component selection
3. Sensor-driven return detection and time-based overdue alert system

---

# 12. Business & Deployment

## Target Users
- Engineering colleges, polytechnic institutes, IoT labs, robotics labs, maker spaces, and school science labs managing shared electronic components.

---

## Estimated Cost

---

## Market Opportunity
- Every technical college in India managing component inventory manually is a potential customer. Scalable from a single 4-box unit to a full lab rack.

---

## Sustainability Considerations
- Reduces component replacement costs, lowers e-waste from lost/damaged modules, and shifts from paper-based registers to digital logs.

---

# 13. Final Demonstration

## Prototype Images

Insert photos.

---

## Demonstration Video Link

---

## GitHub Repository

---

## Presentation Link

---

# 14. Reflection

## What Worked Well?

---

## What Failed?

---

## Key Learnings

---

## Next Steps

* Patent Filing
* Startup Exploration
* Product Development
* Research Publication
* Competition Submission

---

# 15. Final Deliverables Checklist

* Problem Discovery Complete
* User Interviews Complete
* Persona Created
* Problem Statement Finalized
* System Design Complete
* Prototype Demonstrated
* Testing Completed
* Patent Draft Prepared
* Presentation Submitted
* GitHub Repository Updated

---

# MAKERMANIA FINAL PITCH

Each team will present:

1. Problem
2. User Research
3. Insights
4. Solution
5. Prototype Demo
6. Innovation & Patentability
7. Future Roadmap

Presentation Time: 5 Minutes

Q&A: 3 Minutes
