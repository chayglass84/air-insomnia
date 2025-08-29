# air-insomnia
Cam's demo environment for Insomnia


## Spec
Users are identified by a unique email.
Airports - which airports does Air Insomnia operate to and from? Fields are code and optional name.
Planes are individual Aircraft of a certain type. We keep track of the aircraft model, the serial number, and the number of seats on the plane. 
Routes connect a Source Airport and a Destination Airport. They have a calculated length based on the distance between the airports.
FlightPlans are Routes with frequencies and schedules. They operate at a specific time of day, on certain days of the week, with a certain plane.  They are uniquely identified by a Flight Number.
Flights are a specific instance of a specific FlightPlan, on a specific date. 
Tickets let one User book one seat on one Flight.
Therefore, we also need to look up how many Tickets are sold per Flight, how much capacity is left per Flight, and what tickets a User owns.

For example:
A Route is YYZ to YVR.
A FlightPlan is that route being served at 9 AM every weekday, by Flight Number 34, on an Airbus 320 with 100 seats. 
Flight 34 on Aug 15 has 3 Tickets sold, so there are 97 seats left.
