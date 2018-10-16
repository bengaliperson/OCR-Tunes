# OCR-Tunes // Unfinished
GCSE level computer science 2018 project.
Explanation of the code:
Contains Blanks for images.

OCR-Tunes

Success Criteria Decomposition:
Must collect and store data input into it. 
Must be able to create playlists and store songs into playlists.
Must create an account to store the user’s details such as song preferences.
Must store songs under different genres of music.
Must allow the user to change their favourite artist and genre.
Must be able to randomly generate a playlist with different songs of a specific criteria.
Must contain at least 20 songs.
Must have at least 3 different genres.
Must have 5 different artists.
This program could have a logout option as well as a login.
Must be tested. 


Task Breakdown (Functions) :
Log in
Greetings
Does the user have an account?
    Yes, Log in
        Enter Username 
        Enter Password
Create an Account
Create an account:
    Create username
    Check Username is unique
    Create password
Access account
Function: Open file containing user information.
Do username and password match?
# I will create a json file to store all current users and their information.
View all Songs (In alphabetical order and grouped together with 1 artist)
List songs in alphabetical order and show their length.
Create Playlist


View Playlist
Add songs to current playlist
Generate a playlist with random songs under a certain amount of time
Generate a playlist that contains up to 5 songs of a certain artist
Save all songs of a certain artist inside a playlist
Modify account - Favourite genre, Favourite artist.
Create a new function like the one used to create the account but only include the favourite genre and artist.

Pseudo code:

OUTPUT (‘Hello and Welcome’)
SUBROUTINE Login 
	INPUT (“Do you have an account?”)
	IF answer == y
		LOGIN
	ELIF answer == n
		CREATEACCOUNT
	ELSE
		OUTPUT (“Sorry I did not understand’)


Code Development:

1.Log in()
Flow chart:
Function: To check whether the user has an account or needs to create one to access the information. 
Ask the user if they have an account.

Allow the user to input whether they have an account or not.

Output:





2. Access Account()











openusersfile()


Pseudo code-(create account)
OPEN users.json
INPUT new username 
SAVE to users.json
INPUT new password.
SAVE to users.json
INPUT Date of Birth
SAVE to users.json
INPUT favourite artist
SAVE to users.json
INPUT favourite genre
SAVE to users.json


Function: To open the array containing each user’s information so it can be accessed.


createaccount()
Function: Enters the information in an array called ‘users.json’ which will save the login information of all the users.


add_Record(account)
Function: Stores the information in an array.



Output:
This code will allow a new user to create an account and have it stored so they can




3.Login to Account:
Pseudo code-(Login)
Open users.json file
INPUT username
INPUT password
IF username and password match
	ACCESS ACCOUNT
ELSE
	DENY ACCESS
	OUTPUT Does the user have an account?



def Access_Account()
This code asks the user for their username and password and outputs whether they match or not. If the username and password match, the user is taken to the menu system. If the username and password don’t match, an error message is output and the user tries again. The user has an unlimited amount of tries to log in.




def authenticate()
This code checks the username and password and tells the function def Access_Accounts whether the username and password match or not.




Output()
If the user inputs their details right, they are taken to the menu system:


Else, if the user enters their information wrong, they are taken back to the Login() function which gives them a choice to try to login again or create an account:


4.Menu System
Pseudo Code-(Menu System)
OUTPUT- OPTIONS
OUTPUT-What option would you like to add?
IF OPTION =x
	GOTO function x
ELSE
	OUTPUT Sorry I did not understand that.




def menu()
This menu system will ask what the user wants to do with OCRTunes. They have 8 options which include all the criteria demanded.

This will display all the options available to the user. I will add more options to the menu that the user can choose from later on.






Output:

This displays all options and asks the user to choose.
I will add more options later on with the functions that run them.

The following code allows the user to input their choice to use OCRTunes:

Each choice is linked to a specific function which will carry out the task. If the user does not enter a given choice, they are given an error message that will take them back to the start of the function menu() and lets them try again. 







def opensongsfile()
Pseudo code-(List all songs)
OUTPUT Here are all the songs in OCRTunes in alphabetical order.
OUTPUT songs

I have created a json file to store all the songs available for users. 


opensongsfile()
This code will open the json file containing all the songs and can be called at any time. This means that it will save a lot of time as I do not have to re-type this code all the times.














Showallsongs()
I have taken a piece of code from stack overflow to help me write this function  - https://stackoverflow.com/questions/28218173/extract-part-of-data-from-json-file-with-python



And I have modified it to list the songs from my json array:



However this was getting a running error:
It was caused due to the lack of commas at the end of each field in the json file, so I added commas at the end of each field of data except the last one.

I have referenced the songs from where I got them and where I took their information from (E.g length, genre, artist).

Next, I got the error:

The error was caused due to a variable which did not have an attribute to get.
Therefore, I modified the code to fit my json file:

This meant that nearly everything worked. However, I was still getting an error that there was a key error which didn’t accept the ‘Length’ feature of the songs.


I resolved this error by changing all the song lengths from ‘Length(seconds)’ to ‘Length’ which solved the problem. I also removed the spaces between the words ‘Song Name’ as this might cause an error later on due to python not liking spaces in json files. I changed it to ‘SongName’ and removed the space. This meant that my code finally worked.








def Createnewplaylist()
 Pseudo code-(create a new playlist)
OPEN playlists.json
INPUT playlist name
	UPDATE playlists,json
INPUT playlist song
	UPDATE playlists,json
INPUT playlist artist
	UPDATE playlists,json

This function creates a new playlist and asks the user to input the songs they want to store inside the playlist. The playlist is then saved into a json file called ‘playlist.json’ so that they can be later found .

This piece of code asks the user to input the name of their new playlist and adds the record ‘playlist’ in the json file.


This code asks the user to input their song’s name and the artist.

This code is included in the function ‘def Createnewplaylist()’ and will ask over and over for the user to input a song into the new playlist. When the user does not want to add anymore songs to the playlist, they exit the playlist and the playlist is saved into a json file called ‘Playlist.json’, where the user will be able to view it.


This is what the code came up like.



This shows that the playlists can be updated easily and quickly.





def Editinformation()

These are the options that the user can choose from after they have decided to change their information. 
  

This function will change the information that the user has input while signing up to OCRTunes. They will be able to choose the option from the menu system and they will be taken to this function. This function will offer the user two options: 
1.To change the user’s favourite artist 
2.To change the user’s favourite genre 
3. Let the user cancel and go back to the menu.

The output of this code:

The modifications to the json file:



def Viewplaylists():
Pseudo code:
OPEN playlists.json
OUTPUT Here are all the current existing playlists.
OUTPUT Playlists,Songs,Artists.

This code will be able to show all the current playlists that have been created and the songs that are inside the playlists.


I started with this data to list the playlists here and the songs that are inside the playlists. However, it came out with an error that stopped it from running:


This was strange as it was outputting the playlists of the json file with only the first song inside them. It also told me that I had a key error in my json file.
So I checked the json file and found what was causing the error:

This was causing the error due to a playlist having no songs in it. So I removed it.
Then, it worked and came up with:

This meant that the way the songs were saved in the playlists were wrong as it created a new playlist when the user wanted to add another song. This meant that for every song the user adds, a new playlist with the artist’s name. So I will have to change the add playlist function.







Modification of def Createnewplaylist():

This was the old code of the function that created the playlist:



So I solved the problem by creating other functions which added each field to the json file individually; for instance, I will create a function which adds a song, an artist and a playlist. 


This meant that instead of a new playlist being created each time a song was entered, the song was simply added to the end of the playlist. This took a very long time and created more problems than it solved. Therefore, I chose to use the original code and modify it.


I worked out how to make it stop adding so many songs at once to  the json file. The error was caused because I called the function add_record_playlist(playlist) too many times so I changed it to only add the information only once.
This meant that my code worked except that there may be some duplicates in some playlist names; which, due to the time limit, I was not able to solve.

Here is the output of the code:



It creates a new playlist for every new song added which is still acceptable as the user can still save their information about their playlist inside the json file and they can also read the json file and find its information out.



















Flowchart:
Login system.
























Appendix: Code (Python):
import json


def Login():
    print ("Hello and welcome to OCRTunes.")
    Account = (input("Do you have an account?(Y/N)"))
    if Account == ("Y"):
        print ("Log in")
        Access_Account()
    elif Account == "N":
        print ("Create an account")
        createaccount()
    else:
        print ("Sorry, I did not understand that.")
        print ("Please try again.")
        Login()


def openusersfile():
    with open('users.json') as f:
        users = json.loads(f.read())
        return users


def Access_Account():
    username = input("username: ")
    password = input("password: ")
    if authenticate(username,password):
        print("Account found")
        menu()
    else:
        print ("Sorry, no account matches.\n You should try again.")
        Login()



def authenticate(whichName,theirPassword):
    Users = openusersfile()
    for person in Users:
        if (person['Username']== whichName):
            if (person['Password'] == theirPassword):
                return True




def createaccount():
    account = {}
    account['Username'] = input ("Username ")
    account['DOB'] = str(input("Date Of Birth "))
    account['Password'] = str(input("Please enter a Password "))
    account['Favourite_Artist'] = str(input("Favourite_Artist "))
    account['Favourite_Genre'] = str(input("Favourite_Genre "))
    add_Record_Account(account)
    Access_Account()

#def uniqueusername():
#    filecheck = openusersfile()
#    for x in range (len(users.json)):
#        print("{} {}".format(x+1, menu[x]))


def add_Record_Account(account):
    original = openusersfile()
    original.append(account)
    with open('users.json','w') as f:
        f.write(json.dumps(original))




def menu():
    print ("Welcome!\nHere are you options:")
    print ("1.Find song\n2.Create playlist\n3.Edit favourite artist or genre.")
    print ("4.Display all songs.\n5.Generate random playlist with time limit.")
    print ("6.Generate random playlist of 5 songs in a certain genre.")
    print ("7.See all songs from an artist and save them.")
    print ("8.List all genres from OCRTunes.")
    print ("9. View the playlists that you and other users have created.")
    print ("10. Exit")
    choice = input ("Enter your choice: ")
    if choice == "1":
        FindSong()
    elif choice == "2":
        Createnewplaylist()
    elif choice == "3":
        Editinformation()
    elif choice == "4":
        Showallsongs()
    elif choice == "5":
        GenerateTime()
    elif choice == "6":
        Generatefive()
    elif choice == "7":
        Artistsongs()
    elif choice == "8":
        Listgenres()
    elif choice == "9":
        listData()
    elif choice == "10" or "Exit" or "exit":
        Login()
    else:
        print ("Sorry but you may have entered something wrong.")
        print ("PLease try again.")
        menu()


def Generatefive():
    Song = opensongsfile()
    genre = input("Please enter a genre.")
    #matched_genre_songs = []
    #for Song in Songs:
        #if Song ['genre'] == genre:
            #matched_genre_songs.append(song)
    matched_genre_songs = [song for Song in Songs if Song['genre']==genre]
    matched_genre_songs = matched_genre_songs[:5]


def opensongsfile():
    with open('songs.json') as f:
        songs = json.loads(f.read())
        return songs


#def FindSong():
#    Search = str(input("Input the song name using capital letters for each new word. "))
#    input_file=open('songs.json', 'r')

#def Createnewplaylist():
#def Editinformation():


def Showallsongs():
    Songs = opensongsfile()
    SongsArtistOrder = sorted(Songs, key=lambda k: k['SongName'])
    for Songs in SongsArtistOrder:
        print("{SongName}  Artist: {Artist}. Genre:{Genre} Length: {Length} ".format(**Songs))
    menu()



def Editinformation():
    print ("Which information would you like to overwrite:\n Genre or Artist?")
    print ("Press 3 to Exit")
    information = input("Please input the type to change:")
    if information == "Genre" or "genre":
        EditGenre()
    elif information == "Artist" or "artist":
        EditArtist()
    elif information == "3" or "exit" or "Exit":
        menu()
    else:
        print ("Sorry I did not undedrstand this, please try again.")
        menu()



def EditArtist():
    fav_art = input("Please enter your new favourite artist: ")
    original = openusersfile()
    original[0]['Favourite_Artist'] = fav_art
    with open('users.json','w') as f:
        f.write(json.dumps(original)) #Overwrites the old json file.
    menu()


def EditGenre():
    fav_gen = input("Please enter your new favourite genre: ")
    original = openusersfile()
    original[0]['Favourite_Genre'] = fav_gen
    with open('users.json','w') as f:
        f.write(json.dumps(original))
    menu()



def add_Record_playlist(playlist):
        original = openFile()
        original.append(playlist)
        with open('playlists.json','w') as f:
            f.write(json.dumps(original))

def Createnewplaylist():
    playlist = {}
    playlist['Playlist'] = input ("Playlist Name: ") #Asks the user to input their playlist's name.
    def addsong():
        playlist['Song'] = input ("Please input a song inside songs.json: ") #Asks the user to input the song's name.
        playlist['Artist'] = input ("Please input the song's artist.")
        add_Record_playlist(playlist) # Adds the song's name to the playlist.
        addSong= input("Would you like to add another song?(Y/N)") #Asks the user if they would like to add another song to their playlist.
        if addSong == "Y":
            addsong()
        elif addSong == "N":
            menu()
    addsong() #Runs the function addsong() as if this is not there, it will not run.



def openFile():
    with open('playlists.json') as f:
        Data = json.loads(f.read())
        return Data

def listData():
    PlaylistsInfo = openFile()
    for info in PlaylistsInfo:
        print("{Name} has {Song} created by {artist}".format(**info))
    menu()


Login()


