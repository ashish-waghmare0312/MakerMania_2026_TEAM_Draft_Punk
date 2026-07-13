### The days of the workshop so far have been fun and interesting.

# But we went through a variety of phases

## 1. Idea
Our team, [Draft Punk](https://github.com/ashish-waghmare0312/MakerMania_2026_TEAM_Draft_Punk/blob/main/images/Team_Draft_Punk.jpeg), when starting to ideate the product, came to a conclusion about creating an automated component management system for makerspaces.

## 2. Finalization
After many attempts of rethinking, redesigns, and iterations, we finally came to a consensus about which product to finalize. Our product was decided to be the **RFID-based Component Manager** — an intelligent storage solution that uses RFID technology to automatically identify and retrieve components from organized drawers.

## 3. Making
Now we finally come to the part on which the entire bootcamp is based: Making the product.

### a. Building 
We started by designing the shelves using the [layout](https://github.com/ashish-waghmare0312/MakerMania_2026_TEAM_Draft_Punk/blob/main/images/Sensor%20Cupboard%20Layout.jpg) and constructed a modular system with:
- **Frame**: Aluminum extrusion for durability and modularity
- **RFID Readers**: Multiple RFID module sensors positioned at strategic points
- **Microcontroller**: Arduino-based system for initial prototyping
- **Motors**: For automated drawer access and component retrieval

### b. Issues 
The drawers were designed to be made out of [acrylic](https://github.com/ashish-waghmare0312/MakerMania_2026_TEAM_Draft_Punk/blob/main/images/Sensor%20Box.jpg) for transparency and better visibility of components.

However, we encountered several significant challenges:

1. **Locking System Iterations** — We cycled through multiple options:
   - **Solenoid locks**: Initial choice but struggled with consistency and power requirements
   - **Servo-based latches**: Provided better control but had speed limitations
   - Decision: Ultimately selected servo-based latches for reliability and precision

2. **Microcontroller Selection** — We tested and compared:
   - **Arduino Nano**: Limited processing power and memory
   - **Arduino MEGA**: Better performance but larger form factor
   - **ESP32**: Superior connectivity and processing capabilities
   - Decision: Chose ESP32 for its WiFi connectivity and superior performance, enabling remote access features

3. **RFID Accuracy** — Interference from metal cabinet components required careful sensor placement and shielding adjustments (approximately 2-3 days of troubleshooting)

### c. Finishing
We successfully integrated all components into a fully functional prototype. The system now:
- Detects RFID-tagged components automatically
- Opens the appropriate drawer via servo motors
- Logs component access and inventory
- Provides a basic web interface for monitoring

**Key Learnings:**
- **Iterative design matters** — Our multiple prototypes taught us more than rushing to a final design
- **Component compatibility is critical** — Testing microcontrollers early saved us from later integration headaches
- **Physical constraints are real** — Metal shielding around RFID readers was essential and shouldn't be overlooked

**What We'd Do Differently:**
- Prototype the RFID system in the actual cabinet earlier to catch interference issues sooner
- Plan for more robust power management from day one
- Allocate more time for software integration testing

This project successfully demonstrates an automated, RFID-based component management solution that could be scaled for larger makerspaces and educational institutions.
