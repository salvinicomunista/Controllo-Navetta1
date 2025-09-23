# Web Interface for Remote Control of an Omron Shuttle

## Overview
My first internship project involved developing an **intuitive web interface** for **remote control of an Omron shuttle**.  
The work was divided into two main areas:
- **Front-end:** What the user sees and interacts with.
- **Back-end:** The logic and communication behind the scenes.

---

## Problem Identification
This project was born from the observation of a **gap in the automation landscape** for **small and medium-sized enterprises (SMEs)**.  

Most **automated palletizing and handling systems** currently on the market are:
- Extremely **expensive**  
- **Complex** to implement and maintain  
- **Economically viable only for large companies**

As a result, many SMEs remain dependent on **traditional manual methods**, where workers use **forklifts** to transport and stack goods.  
This approach leads to:
- **High safety risks**, including accidents in warehouses
- **Increased labor costs** due to repetitive and low-value tasks

---

## Project Goal
The primary goal was to **propose an intermediate, efficient, and accessible solution**:  
A **user-friendly web interface** that enables remote control of an **Omron shuttle**, acting as an **"autonomous forklift"**.

The system would allow a worker to:
1. Use a **tablet connected to the company network**  
2. Specify the **destination** of the shuttle (e.g., a warehouse, department, or loading area)  
3. Let the shuttle handle the transportation **autonomously or semi-autonomously**

This solution empowers SMEs to **digitally transform their internal material handling processes** without the prohibitive costs of traditional automation systems.

---

## Problems Solved
This project addresses several key issues:

- **Reducing Accident Risks**  
  Automating goods transport minimizes or eliminates dangers associated with forklift operations, improving workplace safety.

- **Optimizing Labor Costs**  
  Personnel can be **reallocated to higher-value tasks**, reducing transportation-related operating expenses.

- **Efficient Resource Management**  
  Fewer forklifts are required, which leads to **better fleet management** and **lower maintenance costs**.

- **Accessible Automation for SMEs**  
  Provides a **realistic alternative** to costly, complex automation systems, making automation feasible for smaller companies.

---

## Web Interface Design
The web interface was carefully designed with a **focus on user experience (UX)**.  
It was divided into **clear sections** to make navigation intuitive and efficient:

- **Home Page**  
  The initial screen displays a **list of available stations**, allowing the user to easily select the shuttle's destination.  
  A **top navigation bar** provides quick access to all other sections of the site.
![amr_home ](https://github.com/user-attachments/assets/13335611-3a42-4596-ba58-a914c5cd3968)
  <br><br>
  


- **Settings Page**  
  Used to **manage main shuttle operations**, including:
  - Sending the shuttle to the charging station
  - Controlling power (on/off)
  - Detailed station configuration
![amr_impostazioni](https://github.com/user-attachments/assets/497bb276-a287-4d1e-b2d4-b214353f782f)
  <br><br>

- **Station Configuration Page**  
  A **subsection of Settings** for adding, editing, or removing stations.  
  Here, users can:
  - Change a station’s **name, location, and ID**  
  - Add **new stations** or remove outdated ones
![amr_configurazioni](https://github.com/user-attachments/assets/4287feeb-de6d-4a97-b1e4-625513b17392)
<br><br>

- **Manual Page**  
  Dedicated to **advanced, manual controls**.  
  Operators can manually activate **specific shuttle actions**, such as:
  - Operating the shuttle’s rollers
  - Running non-standard operations for testing or maintenance
![amr_panello_controllo](https://github.com/user-attachments/assets/0f75c931-9135-4e03-a7d4-03eecc7adc61)

  <br><br>

- **Address Page**  
  Designed for **environments with multiple shuttles**.  
  It allows quick changes to the **IP address** of the currently controlled shuttle, making it easy to **switch between different Omron vehicles**.
![amr_indirizzo](https://github.com/user-attachments/assets/46a76c90-c6e5-456f-83d4-b6116b5d51f6)

  <br><br>
---

## Project Architecture
The solution was built with a **two-layer architecture**, ensuring scalability and maintainability.

### **1. Front-end (User Interface)**
- Developed using **[React](https://reactjs.org/)** – a JavaScript library for creating dynamic, interactive interfaces.
- **[Material-UI (MUI)](https://mui.com/)** was integrated to provide a **modern, responsive, and intuitive design** using pre-built components like:
  - Buttons  
  - Menus  
  - Tables  
  This significantly **accelerated the development process**.

---

### **2. Back-end (Logic & Data Management)**
- Implemented in **Python** using the **[Flask](https://flask.palletsprojects.com/)** framework.
- Flask was chosen for its **lightweight and flexible** nature, making it ideal for building **APIs** (Application Programming Interfaces).
- These APIs serve as the **bridge between the front-end** and the **Omron shuttle**, handling:
  - Command transmission
  - Data retrieval
  - Status updates

---


## Communication with the Shuttle
A crucial part of the project involved **real-time communication** between the back-end server and the Omron shuttle.

- The **MQTT (Message Queuing Telemetry Transport)** protocol was used.
- MQTT is:
  - **Lightweight** and **fast**
  - Optimized for **low-bandwidth and resource-constrained environments**
  - Widely adopted in **industrial automation** and **IoT** contexts

This ensured:
- **Secure and reliable message exchange** between the shuttle and the control interface  
- **Seamless updates** on shuttle status and task execution

---


## Final Objective
Ultimately, my goal was to **make automated internal material handling solutions accessible to SMEs**.  
This project demonstrates how **affordable, modular, and user-friendly technology** can bridge the gap between **traditional manual methods** and **fully automated warehouse systems**.
