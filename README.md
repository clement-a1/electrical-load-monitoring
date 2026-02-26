# Electrical Load Monitoring & Billing System (C++)

This is a simple console-based C++ project that helps calculate electrical energy usage and estimate electricity bills. It allows users to register appliances, store their details, and compute daily and monthly energy costs.

The program is menu-driven and stores data in text files so that records remain available even after closing the application.

---

## What the Program Does

- Register electrical appliances  
- View all saved appliances  
- Search for an appliance by name  
- Calculate total daily energy consumption  
- Estimate monthly electricity cost  
- Save billing summaries to a file  

---

## How Energy is Calculated

Daily energy consumption is calculated using:

```
Daily kWh = (Watts / 1000) × Hours used per day
```

Cost is calculated as:

```
Daily Cost = Total Daily kWh × Tariff
Monthly Cost = Daily Cost × 30
```

---

## Files Used

- `main.cpp` – main source code  
- `appliances.txt` – stores appliance records  
- `billing_summary.txt` – stores saved billing results  

---

## How to Compile and Run

Using g++:

```
g++ main.cpp -o load_monitor
./load_monitor
```

On Windows:

```
g++ main.cpp -o program
program
```

---

## Program Structure

The system uses a structure:

```cpp
struct Appliance {
    string name;
    double watts;
    double hours;
};
```

It also includes:
- Input validation functions  
- File saving and loading functions  
- Energy calculation functions  
- A loop-based main menu  

---

## Input Rules

- Appliance name cannot be empty  
- Power rating must be greater than 0  
- Usage hours must be between 0 and 24  
- Tariff must be positive  
- Invalid inputs are handled safely  

---

## Possible Improvements

- Add edit and delete options  
- Use dynamic arrays (`vector`)  
- Add yearly bill estimation  
- Export data to CSV  
- Add a graphical interface  

---

## Purpose of the Project

This project was developed to practice:
- C++ structures  
- File handling  
- Input validation  
- Menu-driven programming  
- Basic electrical energy calculations  

---

**Author:**  
Electrical Load Monitoring & Billing System  
C++ Console Application Project  

For academic and learning purposes.