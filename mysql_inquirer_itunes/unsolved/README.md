# iTunes Application

Develop a command line tool which stores users information and let's them buy and view their music using Node, MySQL & Inquirer.

## Easier Assignment
* Create a database called itunes.

* Have 3 tables:
	* A songs table that you should populate manually
		* Columns: id, song_title, song_artist
	* A users table
		* Columns: id, name, username, password
	* A pivot table which stores what songs people have bought
		* Columns: id, song_id, user_id
* Pre-populate a songs table as per the sql files attached.
* Inquirer should prompt a choice for the user to "Sign Up" or "Sign in"
* If the user chooses to "Sign In"
	* Check the input username and password against the database.
	* If the username is not in the database, then you can tell the client to sign up and close the connection/inquirer.
	* If the username is in the database, then prompt the user to enter their password.
	* If the password matches the user's account, then prompt them the choices to either:
		* Add a song
			* Then have it prompt what songs are available
		  * Ask them what song they would like to add
		* View the songs that they have
			* Then get their songs from the database

## Difficult Assignment
1. Add a bank to the functionality
	* Create a bank table:
		* id, balance, user_id
	* Every time a user account is created, a bank record is created for that user
	* Add a column to your songs table called 'amount' which will be an INT and give each song a price with a default value of 3
	* When the user adds a song, have it deduce the amount that the song is priced at from the user's balance in the bank table.
	* Add a "View Your Balance" option to the inquirer prompt
		* This should show the user's balance in the bank
2. Use recursion to:
	* Bring the app back to the sign up/sign in prompt if the username or password is incorrect
	* Bring the app back to the user options prompt after a transaction is done
3. Return Errors for:
	* If user forgets to input field for when they sign up
	* if username already exists in the database when they sign up
