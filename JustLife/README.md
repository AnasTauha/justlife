# Getting Started

## Setup Database
In order to run the application please change the username and password of local mysql instance in application.properties file

### JustLife - Test

* [View Documentation](http://localhost:8080/v3/api-docs)
## Project Overview

*Justlife* is an advanced service management platform for coordinating cleaning services, integrating multiple functionalities to handle appointments, professional availability, and vehicle logistics.

### Key Features:

#### Cleaning Professionals:

Available for multiple appointments per day based on their schedule.
Required to take a 30-minute break between consecutive appointments.
Not available on Fridays and operate between 08:00 and 22:00.
The first appointment of the day cannot start before 08:00, and the last appointment must end before 22:00.

#### Vehicles and Drivers:

Each vehicle is assigned a list of 5 cleaning professionals and operates for the entire day.
Vehicles are responsible for transporting cleaning professionals to and from their appointments.

#### Customer Booking:

Customers can book cleaning services specifying:
Start date and time.
Duration (either 2 or 4 hours).
Number of cleaning professionals required (1, 2, or 3).
Cleaning professionals must belong to the same vehicle for a single appointment.

#### Booking Process:

##### Availability Check:

By Date Only: Returns a list of available cleaning professionals and their available times for the specified date.
By Date, Start Time, and Duration: Returns a list of available cleaning professionals who are free during the specified time period.

#### Booking Creation:

Assigns 1 to 3 cleaning professionals to an appointment, ensuring they are from the same vehicle.
Updates the availability of cleaning professionals based on the newly created booking.

#### Booking Update:

Allows modification of booking date and time while updating the availability of involved cleaning professionals.
Justlife ensures efficient scheduling, adherence to professional breaks and working hours, and seamless coordination between vehicles and cleaning professionals, delivering a well-organized and customer-centric cleaning service experience.