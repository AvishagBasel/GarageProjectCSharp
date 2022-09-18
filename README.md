# GarageProjectCSharp

## Objectives
* Integration of Classes, Inheritance and Polymorphism
* Working with Arrays / Collections / Data Structures
* Using Enums
* Development and use of external DII (Assembly)
* Working with numerous projects
* Working with Exceptions

## Exercise
Final objective – Developing a computer software that “manages” a vehicle garage. The system will manage a garage that handles these five types of vehicles -
* Fuel-Based Motorcycle
2 tires with max air pressure of 31 (psi), Octane 98 (fuel), 6.2 liters fuel tank
* Electric Motorcycle
2 tires with max air pressure of 31 (psi), Max battery life – 2.5 hours
* Fuel-Based Car
4 tires with max air pressure of 29 (psi), Octane 95 fuel, 38 liter fuel tank
* Electric Car
4 tires with max air pressure of 29 (psi), Max battery life – 3.3 hours
* Fuel-Based Truck
16 tires with max air pressure of 24 (psi), Soler fuel, 120 liter fuel tank

## The system will supply the user with the following functions:
1. “Insert” a new vehicle into the garage. The user will be asked to select a vehicle type out of the supported vehicle types, and to input the license number of the vehicle. If the vehicle is already in the garage (based on license number) the system will display an appropriate message and will use the vehicle in the garage (and will change the vehicle status to “In Repair”), if not, a new object of that vehicle type will be created and the user will be prompted to input the values for the properties of his vehicle, according to the type of vehicle he wishes to add.
2. Display a list of license numbers currently in the garage, with a filtering option based on the status of each vehicle
3. Change a certain vehicle’s status (Prompting the user for the license number and new desired status)
4. Inflate tires to maximum (Prompting the user for the license number)
5. Refuel a fuel-based vehicle (Prompting the user for the license number, fuel type and amount to fill)
6. Charge an electric-based vehicle (Prompting the user for the license number and number of minutes to charge)
7. Display vehicle information (License number, Model name, Owner name, Status in garage, Tire specifications (manufacturer and air pressure), Fuel status + Fuel type / Battery status, other relevant information based on vehicle type)

## Remarks

1. Design your system in the best manner of code, regarding dividing to classes and
methods, inheritance and polymorphism.
2. Separate between the user interface and the logical layer which manages the object
model and the logical entities of the system (A class like Vehicle should not know the
Console class, not even indirectly) Try and think of solutions for this separation.
3. Place the code which creates new object from the Vehicle class, and only it, in a
separate class, in the logical part of the system. This class may also hold the supported vehicle types list. This class cannot address the user, neither directly, nor indirectly.
4. Design and implement the software in such way in which adding a new vehicle type (i.e. Tractor) in the future will be possible without changing any code (except minor additions in the class from (3) that creates the vehicle objects)
5. Avoid code/logic duplication.
6. You must use:
* List and/or Dictionary
* Enum
* Stringformatting
* FormatException (thrown when an input is not correct regarding Parsing)
* ArgumentException (thrown when an input is not correct logically – for example refueling with the wrong fuel type
* ValueOutOfRangeException - a class you will write – (thrown when an input exceeds the allowed range, for example refueling with too much fuel) This class inherits from the Exception class, and holds additional fields: float MaxValue and float MinValue
