# 8-Bit Jukebox

As the first checkpoint, students will be expected to demonstrate their cumulative knowledge gained throughout the first week of the course. This checkpoint will consist of several requirements of functionality that must be met or exceeded in order to receive a passing grade on this assignment. 

Since we are utilizing the command line and are building a console App, we get that nostalgic video game feel of a time before the graphical interfaces of today. We deemed it only appropriate to create a fun and lively App fitting of those bygone games. Welcome to the 8-Bit Jukebox! This Jukebox will come with some of your favorite melodies inspired from your favorite games. Feel free to find more and add them, or come up with your own!(extension welcome)

## Functionality

Your user should be given a menu that provides the core navigation of your App. From here they should be able to view the JukeBox song collection and have it print out details about the song. They will also need a way of selecting a song to play, which will then set the current song(show some details) and allow them to play it. 

The Main method of the class Program should remain relatively lightweight if possible. The logic and most of the utility of the application should be  moved into the respective classes that make sense. There is not always an exact or specific place these aspects HAVE to go, but there are usually good cases to be made for why they SHOULD go in a specific class. Remember to consider why you are choosing to implement something in a particular way. Considering this goes a long way in preventing future issues, and ultimately makes cleaner, efficient, and easier to read code.

## Classes

### Jukebox

The Jukebox class should contain a bool that tells the program that we are "playing" or accessing the Jukebox. It will also have a list of songs to know which songs are available to play. There will be a method for Setup, which will be called to initialize or set up the state of our Jukebox object(AddSongs, welcome message, in general anything we need to get the state of the object ready to be used). We will have an AddSongs method which will create individual songs and add them to the Songs collection. The last required method we will use is a Play method that should have a way to identify a song to play, taken from user input, and then play that particular song by accessing the individual Song object.

### Song

The Song class should have a unique identifier of some kind, this could be a name or id, anything that can be used by the Jukebox to identify and select the desired Song object. Songs will also contain a list of Note objects. Add some additional properties(times played, description, etc) to create details for the Song to display under the selection process. There will be a play method on the Song object that allows us to play each note that makes up the song.

Console.Beep() is a method that takes in a frequency of the note to play, and a duration of how long to play it for. So, playing a single note looks something like Console.Beep(1080, 500). Our Play method will be utilizing this built in method to play each note.

### Note

The Note class is going to be used to store our Frequency and Duration. The song will use these properties in order to be able to populate the arguments required for Console.Beep().

### Menu(OPTIONAL)

In order to keep the Main method of our program clean and lightweight, it would be nice to utilize a menu class of some kind. As this is an optional class, you can design the structure of this however you like.


## Requirements

User is able to make a song selection from a menu, or if they would like to exit the program. 

Once they have made a selection they should be able to view its details.

They should now be able to choose to play the song.

They should be able to go back to the main menu. HINT: This would likely be a submenu off of the main menu.


### Additional

If you feel ambitious, you could reorganize the structure so that you first choose an album that the songs might be contained within and create a menu interface for that as well.
