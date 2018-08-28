1. To-Do List
This app will be an app for tracking and managing tasks. Not only will it keep track of whether tasks have been completed, it will also keep track of how long each task took to complete. Tasks can be grouped into 'projects' to keep them organized.

My data model for a to-do list app would look like this :

let projects = {
houseCleaning : {
    taskDescription = "Mop"
    completed = false
    date = "08/27/18"
}
makeStew: {
    taskDescription ="Buy ingredients"
    completed = "false
    date = "08/27/18"
}
}

Answer here:
I would use those properties because this will allow the user to see the description of the task and whether it is completed or not as well as what day it should be completed. 
It would also allow the program to be able to add the task to the "completed" array based on the "completed" property.


2. Photo Sharing App
In this app, users can upload photos to their accounts and share them with others. These photos can be grouped into albums.

My data model for the Photo Sharing App would look like this:

{
Users {
johnsPhotos : {
    photos: [photo1.jpeg, photo2.jpeg, photo3.jpeg]
    familyPhotos: [babies1, thanksgiving, christmas]
}
}
AllPhotos : {
photos: [every.jpeg, photo.jpeg, that.jpeg, exists.jpeg]
}
}

Answer here:
I set each user within a "Users" object that contains object's with the user's username, a photos parameter as well as a parameter that uses the album name as the key and an array of photos as the value.
I would also have anothr object within the app that holds every photo (via an array) being stored on the app's database.


3. Home Automation Manager
This app will be a tool for managing a home automation system; it will keep track of the time and temperature of the house that it monitors, and use that information to turn on and off different lights and adjust the thermostat up and down.


My data model for the Home Automation Manager would look like this:
{
JohnsHouse: {
    Settings: {
        temperature: 97
        time: "0200"
        lights_on: true
}
KatherinesHouse: {
    Settings: {
    temperature: 1
    time: "1300"
    lights_off = false
}
}
}


Answer here
I would set objects within an overall object with each object containing the "name" of the specific house that has specific settings for the aforementioned house.
These settings include the temperature and time as mentioned in the instructions and a property that checks for whether the lights are already on/off.

4. Sneaker Store
This app will allow customers to browse a list of products (sneakers, in this case), add those products to a cart, and save that cart as a past order once the purchase is complete.

My data model for the sneaker store would look like this:

var shoesInventory = {
Shoes: {
Jordan :{
    price: 85
    quantity: 1
    size: [11,12,13]
    }
    Sketchers: {
    price: 12
    quantity: 3
    size: [ 11,12,13]
}
}
var customerAccounts = {
    Johnny : {
        customerCart:  [ Jordan, Sketchers]
        orderHistory: [ ]
}
Sue: {
        customerCart: [Sketchers]
        orderHistory: [Jordan]
}


}

Answer here:
I would create an object for shoes that contains other objects detailing the shoe's name, the available shoe sizes, as well as remaining quantities.
The "Users" portion would contain the name of each user as the object name, a "customer cart" for each user which contains the items they would like to purchase as well as a "order history" array that contains items they have purchased in the past.


Representing Abstractions in Code
Once you've chosen the abstractions that your app will use, the next step is to figure out how to actually represent those abstractions in code. The same abstraction can often be represented in multiple different ways, and there may be trade-offs in speed and simplicity that come from using one representation vs another.

5. Subway System
The advantage of using this data model is that it is not saturated with a lot of properties that make the data a feat to read.
On the contrary, a disadvantage of this model is that it does not allow the user to see which lines are available at a certain station.
Also, the locations are in the description instead of there being a property that effectively shows stations/lines by location.


6. Doctor Appointment App
In this example, I immediately gravitate towards the second option as the better solution simply because the purpose of the app is to allow both the doctor and the patient to be able to easily view the appointments that correspond to them and the second option achieves that purpose.

It creates an "appointment" parameter that contains the information of both the patient and the doctor that will be easier to display in a UI but moreso will be easier for the developer to read since it is centered around appointments and which doctor/patient pair correspond to it(I think). 

The first option seems that it would be better for just doctor's since it shows pertinent information to upcoming appointments under their own object.
Perhaps a system administrator would also enjoy the first option as well as it would allow them to filter appointments by the doctors name.

7. Tic-Tac-Toe
You've been tasked with building an in-browser tic-tac-toe game.

a. What are some possible entities that your application might use to model its data? Please pick at least two, with at least two properties apiece.

Answer here
I would use: 
var user = {
Johnny: {
    moves = [ ]
    wins = 0
    }
}

var gameTrophies = {
    champion = ''
    numberOfUsers = [ ]
}



b. How might those entities be represented in JavaScript code?

var gameTrophies = function(champion,numberOfUsers){
this.champion = champion
this.numberOfUsers
}

var newUser = function(name, moves, wins){
this.name = function name() {
this.moves = moves
this.wins  = wins
}
    }

Answer here

c. Justify your choices in a) and b). Why these entities? Why these representations?

Answer here
I chose "champion" and "numberOfUsers" because they represent realistic game features. The properties in game features track who is the current champion and also who has an array of all online users (which will show how many there are in the navigation bar).

I chose name as an "outer object" that contains the properties moves and wins to track the player's moves and how many "wins" are currently under their belt.
