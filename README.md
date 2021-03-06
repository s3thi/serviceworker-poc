# serviceworker-poc

serviceworker-poc is a simple application that demonstrates the ServiceWorker
API. It lets you list a user's GitHub repositories by typing their username
into a search box, and caches the list of repositories for offline access.

**NOTE:** this project uses several ES6 and ServiceWorker features that are
only available in Chrome Canary and Firefox Aurora (or Firefox Developer Edition)
as of this writing. Things might behave badly or break entirely in older
browsers.


## Running

First, clone this repository:

	$ git clone https://github.com/GeneralMaximus/serviceworker-poc

Then, `cd` into the project directory and install all the dependencies:

	$ cd serviceworker-poc
	$ npm i

Finally, run the application:

	$ npm start


## Demonstration

1. With the server still running, open http://localhost:3000 in your browser.
   After the page has loaded, refresh it using Cmd+R/F5 once so that the
   ServiceWorker can begin listening to events.
2. Enter a valid GitHub username in the search box and click "search". The
   application will display a list of repositories belonging to the user.
3. Repeat step 2 for as many users as you like. Each time you look for a new
   user, the application caches the result for offline viewing.
4. Disable the network connection on your computer.
5. Now, go back and search for the same usernames you searched for in
   steps 2 and 3. Despite the lack of a network connection, the application
   still shows you the cached search results.
