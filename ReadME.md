# XSS 

  Cross-script vulnerability

## Getting Started

	Install the project's dependencies using npm:

	npm install
	
	Now we can run the local web server using Node.js:

	node server.js

## XSS Proof of concept

	Open the browser and run the URL below

	http://localhost:3000/?username=%3Cimg%20src%3D%22no%20url%22%20onerror%3D%22alert(%27your%20logged%20in%27)%22%3E
	
	And now open console and press F12 and you can move to the tab cookies and can see the cookies been saved.
	The browser url been saved and there it is possible to access via XSS vulnerability.
	
	If you try to access the URL, complete script and name is available in the form of javascript code.
	
	Because in the function named function ###showLoggedResults we should not use string interpolation, that is the culprit of vulnerability. 

    #Fixing

    Change the Javascript function ###showLoggedResults, use to pre append text as mentioned in the index-fix.html

	
### sources

    - https://www.tutorialspoint.com/nodejs
	 
	- https://github.com/Learn-by-doing/xss

    

