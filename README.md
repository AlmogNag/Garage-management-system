## Garage Management System

A C# console application that models a garage and common operations on vehicles (cars, motorcycles, trucks), including tire operations, refueling/recharging, and status tracking.


## Features

* Register vehicles and manage their lifecycle in a garage (via GarageManager).
* Support for multiple vehicle types:
  - Car (Car, FuelCar, ElectricCar)
  - Motorcycle (Motorcycle, FuelMotorcycle, ElectricMotorcycle)
  - Truck (Truck)
* Common vehicle data model (Vehicle) with composition of Tire.
* Fuel/Electric energy models and enums (FuelType, ElectricType, Enums).
* Factory/creation utilities (VehicleCreator) for building vehicles.
* Console entry point (Program.cs).


## Project structure
.
├─ Program.cs
├─ GarageManager.cs
├─ VehicleCreator.cs
├─ Vehicle.cs
├─ Car.cs
├─ Motorcycle.cs
├─ Truck.cs
├─ Tire.cs
├─ FuelCar.cs
├─ ElectricCar.cs
├─ FuelMotorcycle.cs
├─ ElectricMotorcycle.cs
├─ FuelType.cs
├─ ElectricType.cs
├─ Enums.cs
├─ Constants.cs
├─ ValueRangeException.cs
└─ Vehicles.db   (data file in repo)

The file list above reflects the repository’s root contents. 

--- 

## Usage

* Run the application.
* Follow the console prompts to:
  - Add/register vehicles (cars, motorcycles, trucks).
  - View/update vehicle status (e.g., “in repair”, “repaired”, etc., based on your enum definitions).
  - Inflate tires to maximum pressure.
  - Refuel or recharge according to the vehicle’s energy type.
  - Inspect vehicle details.


## Sample Run

=== Garage Management System ===
1) Register new vehicle
2) Inflate tires to max
3) Refuel vehicle
4) Recharge vehicle
5) Change vehicle status
6) Show license numbers (filter by status)
7) Show vehicle details
8) Exit
   
Select option: 1

-- Register new vehicle --
Enter license number: 12-345-67
Owner name: Alice
Owner phone: 052-1234567
Select vehicle type:
  1) Fuel Car
  2) Electric Car
  3) Fuel Motorcycle
  4) Electric Motorcycle
  5) Truck
Choice: 1
Car model: Honda Civic
Number of tires: 4
Tire manufacturer (all): Michelin
Initial tire pressure (0-32): 28
Max tire pressure (per tire): 32
Fuel type (e.g., Octane95/Octane98/Diesel): Octane95
Current fuel amount (liters): 30
Max fuel capacity (liters): 45

Vehicle 12-345-67 registered successfully.
Current status: InRepair

[Enter to continue]

=== Garage Management System ===
1) Register new vehicle
2) Inflate tires to max
3) Refuel vehicle
4) Recharge vehicle
5) Change vehicle status
6) Show license numbers (filter by status)
7) Show vehicle details
8) Exit
   
Select option: 2

-- Inflate tires --
Enter license number: 12-345-67
All tires inflated to their maximum pressure.
[Enter to continue]

=== Garage Management System ===
Select option: 3

-- Refuel vehicle --
Enter license number: 12-345-67
Fuel type: Octane95
Amount to add (liters): 10
Refuel completed. Current fuel: 40.00 / 45.00 L
[Enter to continue]

=== Garage Management System ===
Select option: 5

-- Change vehicle status --
Enter license number: 12-345-67
Select new status:
  1) InRepair
  2) Repaired
  3) Paid
Choice: 2
Status updated to 'Repaired'.
[Enter to continue]

=== Garage Management System ===
Select option: 6

-- Filter licenses by status --
Show vehicles with status:
  1) InRepair
  2) Repaired
  3) Paid
Choice: 2
Licenses:
  • 12-345-67
[Enter to continue]

=== Garage Management System ===
Select option: 7

-- Vehicle details --
Enter license number: 12-345-67
License: 12-345-67
Owner:   Alice (052-1234567)
Type:    Fuel Car — Honda Civic
Status:  Repaired
Energy:  Fuel (Octane95) 40.00 / 45.00 L
Tires:   4 × Michelin — Pressure: 32/32 PSI (max)
[Enter to continue]

=== Garage Management System ===
Select option: 8
Goodbye.
