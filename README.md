# friends

1. Eclipse -- > spring-boot:run
2. To run from command line :  mvn spring-boot:run ...pls setup maven path and java if not setup allready
2.1 https://www.mkyong.com/maven/install-maven-on-mac-osx/ maven path for mac


Creating New Record:
/booking/create?psngrName=Dinesh&departure=Noida&destination=Pune create a new booking with an auto-generated.

For Example:
http://localhost:8080/booking/create?psngrName=Vinesh&destination=Delhi&departure=Farrukhabad
{
• booking:
{
o id: "57abe8d42ca52424e8e88027",
o psngrName: "Vinesh",
o departure: "Farrukhabad",
o destination: "Delhi",
o travelDate: 1470884052977
},
• message: "Booking created successfully",
• status: "1"
}

Reading a Record:
/booking/read?id=[bookingId]: Read the booking with the passed bookingId.

For Example:
http://localhost:8080/booking/read?bookingId=57abe8932ca52424e8e88024
{
• booking:
{
o id: "57abe8932ca52424e8e88024",
o psngrName: "Arnav",
o departure: "Pune",
o destination: "USA",
o travelDate: 1470883987113
},
• message: "Booking found successfully",
• status: "1"
}

Updating a Record:
/booking/update?bookingId=[bookingId]&psngrName=Sweety: Update the booking for a given booking id.

For Example:
http://localhost:8080/booking/update?bookingId=57abe8a72ca52424e8e88025&psngrName=Anamika
{
• booking:
{
o id: "57abe8a72ca52424e8e88025",
o psngrName: "Anamika",
o departure: "Noida",
o destination: "USA",
o travelDate: 1470884007369
},
• message: "Booking updated successfully",
• status: "1"
}

Read All Records
http://localhost:8080/booking/read-all
{
• totalBooking: 5,
• message: "Booking found successfully",
• bookings:
[
o {
 id: "57abe8322ca52424e8e88023",
 psngrName: "Dinesh",
 departure: "Noida",
 destination: "Pune",
 travelDate: 1470883890814
},
o {
 id: "57abe8932ca52424e8e88024",
 psngrName: "Arnav",
 departure: "Pune",
 destination: "USA",
 travelDate: 1470883987113
},
o {
 id: "57abe8a72ca52424e8e88025",
 psngrName: "Sweety",
 departure: "Noida",
 destination: "USA",
 travelDate: 1470884007369
},
o {
 id: "57abe8bf2ca52424e8e88026",
 psngrName: "Adesh",
 departure: "Kannauj",
 destination: "Noida",
 travelDate: 1470884031444
},
o {
 id: "57abe8d42ca52424e8e88027",
 psngrName: "Vinesh",
 departure: "Farrukhabad",
 destination: "Delhi",
 travelDate: 1470884052977
}
],
• status: "1"
}

Deleting a Record:
/booking/delete? bookingId=[bookingId]: Delete a booking for given booking id.

For Example:
http://localhost:8080/booking/delete?bookingId=57ac0d681ff9b3117caf7c85
{
• message: "Booking deleted successfully",
• status: "1"
}
