# PLC-Traffic-Light
simple PLC Crossroad Traffic Light

## Project Description

This PLC project simulates a **traffic light control system** for a four-way intersection.

![Traffic-light-controlled-crossroad1](https://github.com/user-attachments/assets/56ee92ea-4ecc-4139-8baa-921053c6189a)


### Logic Overview

- **Network 1** controls **Green 1**, **Yellow 1**, **Green 2**, and **Yellow 2** lights.  
  When the simulation starts, **Green 1** turns on for **7 seconds**, followed by **Yellow 1** for **3 seconds**.  
  During this time, **Red 2** remains ON to stop the other direction.

- After **Yellow 1** turns off, **Green 2** turns on for **7 seconds**, then **Yellow 2** for **3 seconds**.  
  While **Green 2** and **Yellow 2** are active, **Red 1** is ON.

- Once **Yellow 2** finishes, a **20-second timer** activates, during which **both 1 and 2 directions** are **red**.  
  This ensures that all directions stop before switching to the next phase.

- **Network 4** works similarly to **Network 1**, but with a timer placed at the beginning instead of the end.  
  (This timer also runs for **20 seconds**.)

### Control Mechanism

- While **directions 1 and 2** are operating, **directions 3 and 4** remain stopped.  
- When **directions 3 and 4** are active, **1 and 2** stay red.  

This mechanism ensures smooth traffic flow and prevents intersection blocking.




