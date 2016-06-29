# Web-Services

As part of a part of a project we were required to build 4 web services. Two were to be developed by using traditional call by value structure. While the other two were to be developed using RESTful web service guidelines and for the services to be called via web URL invocation and parameter passing through the URL itself. Afterwards it would fetch the result using web get fuction calls. Then we were tasked to build a clean and simple testing webpage, so graders have a simple environment to test our services. We were expected to incorporate the published web services by publishing the web services onto a hosting server so they could be accessed remotely. We were also required to follow the principles of server sided scripting as opposed to client sided scripting so that user inputs and executions are more secure and seamless. And finally the webage was required to follow basic UX and UI guidelines such that an ordinary user can navigate it with ease. Below are examples of each of the web services' fuction, our group had designed each of these functions around the theme of a travel based website.

**Service One: Print Continent Population Upon User Input**
The fuction of this web service was designed so the user can enter a string input of a country name such as "North America" and the web service would take the input and send it to the hosting server and after the function would be evaluated it will send the result back to the webpage GUI.

This was designed to be a RESTFul Service as well and was invoked using the following call
```
[WebGet(ResponseFormat=WebMessageFormat.Json,UriTemplate="population?input={input}")]
```
"Input" on the URL was to be user input of a continent so invocation from the webpage would be along the lines of  http://hostingserver.com/population?input=Africa

**Service Two: Print a Randomized Password Upon User Input of Desired Password Length**
The fuction of this web service was to create a simple and user friendly way to create strong, complex, and secure passwords. The user would enter a desired password length which is sent to the hosting server. The hosting server will then send the weboage GUI an output of a randomized password as per given length.

This was designed to be a RESTFul Service as well and was invoked using the following call
```
[WebGet(ResponseFormat = WebMessageFormat.Json, UriTemplate = "password?passwordLength={passwordLength}")]
```
"passwordLength" on the URL is supposed to be the user input the webpage accepts and then invokes the URL by using the given parameter of the input along with the URL. The invocation is along the lines of
http://hostingserver.com/password?length=8
