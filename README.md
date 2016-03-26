## HTTP Questions

__URLs__

* Name all of the parts of the url that you can remember.  In your own words describe what they do.
* ```protocol, domain, port, query string. protocol refers to whether the website is secure or not (hhtp vs https), domain names are created for human viewing to make it clear what web page the user wants to navigate to, the port is usually invisible to the user, but is attached to every domain. default ports are attached for either secure or insecure webpages. The path is the object path to the file in which we want to view. http://www.website.com/us/stuff/files as an example, everything after the first "/" is the filepath. Query strings are defined by a /? followed by a collection of keys and values relating to data within a webpage```
* Name the pieces of the following urls:
	* `https://www.google.com/` || ```https is the protocol, www.google.com is the domain name, which is for humans to recognize what web page they want to navigate to```
	* `https://workbook.galvanize.com/cohorts/41/learning_experiences/367` || ```https is the protocol, workbook.galvanize.com is the domain, the port is invisible to the user but being implimented by the browser, and cohorts/41/learning_experiences/367 is the pathway ```
	* `http://locahost:5000/animals/puppies?onlycute=1&size=medium#firstpuppy` || ```http is the protocol, localhost is the domain, 5000 is the port, /animals/puppies is the pathway to the query string, /?onlycute=1&size=medium is our query string, with keys a, and #firstpuppy is an anchor that should take us directly to a specific part of the page that we've searched for```
	* `https://en.wikipedia.org/wiki/List_of_HTTP_status_codes#4xx_Client_Error`
* Can a server use more than 1 port?```yes, each port represents	a different pathway for certain types of data```
* Why is https different than http?```https refers to a secure protocol, while http is an unsecure protocol```
* How does a server interpret the following url's query paramter.  What data structure does it create on the server?```the server will interpret the query parameters as the key of puppies with the value of fido, the value of max, and the value of moxie. it will return an object with those keys and values```

```
http://locahost:5000/animals?puppies=fido&puppies=max&puppies=moxie
```

__HTTP Request/Response__

* Name at least 4 http verbs
* ```get, post, delete, put```
* What is each verb useful for in your own words
* ```Get is how we request info from the server in regards to viewing a page. Post is used for sending data to a server from the client. delete is removing data from the server that the user/client has inputted. Put helps the user edit data that is already on the server```
* What does idempotent mean?
* ```idempotent refers to a "safe" method, meaning it must only be used to retrieve info or data from a server  ```
* Name the 5 http status code ranges.  What are they used for in general?
*  ```100, 200, 300, 400, 500. 100 refers to the correct things happening in terms of client/server interaction. 200 means that the interaction was successful! 300 refers to redirects, 400 refers to client-side errors, 500 refers to server-side errors ```
* If a server returns a http status code of 301 and a location of `https://www.google.com/`, what does the browser do?
* ```The browser will redirect you to the new URL of whatever website you were trying to reach. ```
* For the following HTTP headers, decide if the following header is used for requests, responses or both:
	* Accept```request```
	* Content-type```both```
	* User-agent```request```
	* Set-cookies```response```
	* Cache-control```response```
	* Cookie```request```
* Is the following a http request or response?  How do you know for each?

```
HTTP/1.1 200 OK
Access-Control-Allow-Origin: *
Vary: Accept
Content-Type: text/html; charset=utf-8
Content-Length: 722
ETag: W/"2d2-Wu0We9N5g35FXWY+gOATLA"
Date: Tue, 08 Mar 2016 20:37:11 GMT
Connection: keep-alive

<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <link rel="stylesheet" href="/style.css">
    <title>Student Roster</title>
  </head>
  <body>
    <main>
      <h1>Student Roster</h1>
    
        <section>
          <h3>Daenerys Targaryen</h3>
          <span>Student Id: nys8fbohl</span>
          <h4>Hobby: Motherhood</h4>
          <img src="https://i.imgur.com/KlycRG5.jpg" alt="Daenerys Targaryen" />
        </section>
      
        <section>
          <h3>Tyrion Lannister</h3>
          <span>Student Id: njehukbohe</span>
          <h4>Hobby: Traveling</h4>
          <img src="https://i.imgur.com/fFMusdC.png" alt="Tyrion Lannister" />
        </section>
      
    </main>
  </body>
</html>
```
``` ```The example above me is a response, we can tell because there is HTML under the AJAX text```

```
DELETE /students/n1vmyrw3x HTTP/1.1
Host: g22-students.herokuapp.com
Accept: application/json
Cache-Control: no-cache
Postman-Token: 0041e3c3-efdb-f0c3-b2f4-2d79f6d0f44b
```
```The example above this text is a delete request, because it is listed as a "delete" method, and there is no data following it ```
__JSON__

* Describe what JSON is.  What is it used for.
* ```JSON stands for Javascript Object Notation, which is the core data exchange format for the internet. It creates a string, containing an array of objects with keys and values, similar to an object in Javascript```
* Convert the following map into a javascript object then console log the age.

```
{"company" : "Github", "age": 7, "categories" : "Services,Internet,Software"}
```
* Convert the following to a javascript object.  Console log each company name.

```
{ "Companies":[ { "company": "Github", "age": 7, "categories": "Services,Internet,Software"},
              { "company": "Airbnb", "age": 6, "categories": "Hotels,Travel"},
              { "company": "Square", "age": 7, "categories": "FinTech,Hardware + Software,Finance"},
              { "company": "Dropbox", "age": 11, "categories": "Cloud Data Services,Storage,Web Hosting"}
            ]
}
```
```var myObj =JSON.parse('{ "Companies":[ { "company": "Github","age"7,"categories":"Services,Internet,Software,
{ "company": "Airbnb", "age": 6, "categories": "Hotels,Travel"},{ "company": "Square", "age": 7, "categories": "FinTech,Hardware + Software,Finance"},
{ "company": "Dropbox", "age": 11,"categories": "Cloud Data Services,Storage,Web Hosting"}]})
``` 
```console.log(myObj[0]);```






* The following is javascript.  Convert the object to a string and console log it.

```
var myObj = {
  company: "Galvanize",
  age: 3,
  categories: "Education"
};
```
```JSON.stringify({ company: "Galvanize"", age: 3, categories: "Education"});
console.log(myObj);
```
__MISC__

* Describe what DNS is.```DNS translates ip addresses for servers to easy-to-read domain names for human use```
* In the terminal, type `man curl`.  Look at the man page for curl.  What do the following flags do? `-v`, `-X`.  (Hint: to search for a string, type `/` then the text you want, then enter.  To quit the man page, type `q`).

```-v is still the verbose tag we are used to seeing, and -x is to use a proxy``

* What is TCP/IP?  How does it interact with HTTP?

```TCP/IP runs under HTTP and interacts with DNS```

* Does HTTP break the data that is being sent into small packets?  If not, what protocol is responsible for it?
* ```TCP/IP is responsible for sending packets, so is UDP```
