Initial Notes from Requirements Gathering
Imagine that you have captured the following notes from an initial interview with the client, Rodney Ridealot, the owner of Bend Bike Shop.

Bend, Oregon is a small town situated on in Central Oregon. Because of its proximity to the Deschutes River and civic improvements it has seen growth in tourism. Recreational biking, along the Deschutes River, is a popular activity. The Bend Bike Shop rents bikes on a daily/hourly basis and has seen growth so that an automated system for rentals and other management functions is needed. What is desired is a web-based system where customers can reserve and pre-pay for bike rentals. Kiosk stations will be available in the store for customers that have not made advance reservations. This system must also handle inventory management for the bikes. 

Bikes available for rental have a number of characteristics to accommodate a wide variety of customers – including young adults interested in higher performance biking, older adults wanting a more comfortable biking experience, bikes for children, and other special needs bikes. To accommodate the bicyclist needs, the system must be capable of displaying an inventory of available bikes. The customer must be able to search the inventory for available bikes matching search criteria. The customer must be able to select a group of bikes for rental on a given day. To complete the transaction the customer enters credit card information and other personal data. The credit card is not charged until after the bikes are returned. 

The in-store kiosk stations function the same as the general web-based interface with the exception that they have a credit card swipe capability so that the customer does not need to key in their credit card information. All rentals require a valid credit card. Store employees are available for customers requiring assistance at the kiosk stations. Reservations may be changed or cancelled until 24 hours before the scheduled rental time. 

Upon return of a bike the duration of the rental is noted and compared to the requested rental duration. The final rental charge is determined and the credit card is charged. Store employees record any problems with bikes upon their return. A returned bike is out of service until it has been inspected by a store employee. A late fee is assessed if the bike is returned more than 30 minutes after the requested rental return. The late fee is reduced if the renter phones the store to notify that the rental will be late. 

Management must be able to set the charge for reservation changes and cancellations. Management must also be able to set the bike rental rates. Typically rates reflect seasonal variations in bike usage. However, rates must also be able to be changed to reflect holidays and other events. Bike rental rates are set by the type of bike – performance, recreational, or other. 

Management also must be able to take bikes out of service for maintenance and be able to add bikes to the inventory. Adding a bike to the inventory requires entering data to the system to describe the bike. 

Various reports are needed from the system, such as a summary report describing the inventory and summary reports of rental history for the inventory. The system must also be able to report on the rental history for individual bikes, noting how often the bike has been rented and any problems recorded during inspection and maintenance.

No return -> 7  days -> they become blacklisted from renting again? Blacklist field in customer table?
Customer account access / creation with reservation history

seasonal rates change 

user reviews via email

Customer table:
CustomerID
CustomerName
CustomerPhone
CustomerEmail
CustomerPaymentInfo, no amex
CustomerBlacklisted
CustomerRental: up to 7 days, then re billed if they want to keep it longer

Bike table:
BikeID
BikeType: mountain bikes, hybrid bikes, kids, road
WheelSize
FrameSize
BikeStatus
BikeRentalHistory
BikeInspectionHistory

Rental table:
RentalID
RentalCustomerID
RentalBikeID
RentalStartDate
RentalEndDate
RentalStatus

Inventory table:
InventoryID
NumberOfBikes
NumberOfBikesAvailable
NumberOfBikesRented
NumberOfBikesInService
NumberOfBikesByType

goal may or june for the project
