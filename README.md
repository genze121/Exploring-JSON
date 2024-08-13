<h1 style="text-decoration:underline">JSON - Introduction</h1>

<ul>
  <li>JSON stands for <span style="color:tomato;font-weight:700">Javascript Object Notation</span>.</li>
  <br/>
  <li>The JSON format was originally specified by
  <a href="https://www.crockford.com/slides.html" target="_blank">Douglas Crockford</a>.</li>
  <br/>
  <li>JSON is generally used to exchange or interchange data.</li>
  <br/>
  <li>JSON is light-weight and easy to understand and easy to use.</li>
   <br/>
  <li>JSON is basically used to transmit data from client to server or server to client.</li>
  <br/>
   <li>File extension of JSON is ".json".</li>
    <br/>
   <li>The MIME type for JSON text is "application/json".</li>
   <br/>
   <li>JSON is language independent. Mostly all the languages supports JSON.</li>
</ul>

<h1 style="text-decoration:underline;text-underline-offset:8px">JSON Syntax</h1>

<ul>
<li>Data is represented in name/value or key/value pairs.</li>
<br/>
<li>Data is separated by comma.</li>
<br/>
<li>A name/value pair consists of a field name (in double quotes), followed by a colon, followed by a value:</li>

```json

"name":"JavaScript"

```
<br/>
<li>JSON can be represented using two ways. They are as follows:-</li>
</ul>

1) Using curly brackets.

```json

{
  "name":"John",
  "age":30,
  "city":"New York"
}

```

2) Using Arrays.

```json

[
  {
    "name":"John",
    "age":30,
    "city":"New York"
  },
  {
    "name":"Mohan",
    "age":25,
    "city":"Delhi"
  }
]

```

<h1 style="text-decoration:underline;
text-underline-offset:8px">JSON Datatypes</h1>

<p>JSON supports following datatypes. They are as follows:-<p>
<ul>
 <li>String</li>
 <li>Boolean</li>
 <li>Object</li>
 <li>Arrays</li>
 <li>null</li>
 <li>Number</li>
</ul>

<div style="background-color:#ffdddd;border:1px solid gray;border-radius:10px;padding:10px;box-shadow:3px 3px aqua;color:#000">
 <b style="text-decoration:underline">Note:-</b> JSON values <b>cannot</b> be one of the following data-types. They are as follows:-
 
  <br/>

  1) function
  2) date
  3) udefined
</div>

<h1 style="text-decoration:underline;text-underline-offset:10px">Examples of JSON Datatypes</h1>

1) String

```json

{
  "name": "Javascript"
}

```

2) Boolean

```json

{
  "isEmployee":true
}

```

3) Object

```json

{
  "employee":{
    "name": "JSON",
    "isEmployee":true,
  }
}

```

4) Arrays

```json

{
  "fruits":["mango","apple","pineapple","banana"]
}

```

5) null

```json

{
  "name": null
}

```

6) Number

```json

{
  "mobileNumber": 1234567890
}

```

<h1 style="text-decoration:underline;">Difference Between JSON and XML</h1>

<table>
  <tr>
    <th>JSON</th>
    <th>XML</th>
  </tr>
  <tr>
    <td>JSON stands for Javascript Object Notation. </td>
    <td>XML stands for Extensible Markup Language.</td>
  </tr>
  <tr>
    <td>JSON is simple to read and write.</td>
    <td>XML is less simple than JSON. </td>
  </tr>
   <tr>
    <td>JSON is easy to learn.</td>
    <td>XML is less easy than JSON. </td>
  </tr>
   <tr>
    <td>JSON supports array.</td>
    <td>XML doesn't supports array. </td>
  </tr>
   <tr>
    <td>JSON doesn't provide display capabilities.</td>
    <td>XML provides display capabilities because it is a markup language. </td>
  </tr>
  <tr>
    <td>JSON is less secured than XML.</td>
    <td>XML is more secured than JSON. </td>
  </tr>
  <tr>
    <td>JSON files are more human readable.</td>
    <td>XML files are less human readable. </td>
  </tr>
  <tr>
    <td>JSON supports only text and data.</td>
    <td>XML supports many datatypes such as text, number, charts, graphs etc. Moreover XML offers for transferring the format or structure of the data with the actual data. </td>
  </tr>
</table>

<div style="background-color:#ffdddd;border:1px solid gray;border-radius:10px;padding:10px;box-shadow:3px 3px aqua;color:#000">
 <b style="text-decoration:underline">Note:-</b> JSON doesn't support comments. It is not a standard. But there is one way to represent comments in JSON by using an attribute "comments".
 Here is an example for your reference:-

  ```json

{
  "name":"John",
  "age":30,
  "comments": "This is a comment in JSON"
}

  ```

Note:- Here, <b>"comments"</b> attribute is treated as comment.
</div>

<h1 style="text-decoration:underline;text-underline-offset:8px"> Accessing JSON Object</h1>

<ul>
  <li>JSON can be accessed in two  ways. They are as follows:-</li>
</ul>

1) Using dot (.)

```javascript

const jsonObject = {
 "name":"JSON",
 "age":30,
 "mobileNumber":1234567890,
 "isManager":false,
 "isEmployee":true,
 "salary":60000
}

console.log(jsonObject.name);
console.log(jsonObject.age);
console.log(jsonObject.mobileNumber);
console.log(jsonObject.isManager);
console.log(jsonObject.isEmployee);
console.log(jsonObject.salary);

```

2) Using square bracket [""]

```javascript

const jsonObject = {
 "name":"JSON",
 "age":30,
 "mobileNumber":1234567890,
 "isManager":false,
 "isEmployee":true,
 "salary":60000
}

console.log(jsonObject["name"]);
console.log(jsonObject["age"]);
console.log(jsonObject["mobileNumber"]);
console.log(jsonObject["isManager"]);
console.log(jsonObject["isEmployee"]);
console.log(jsonObject["salary"]);

```
<h1>JSON.parse()</h1>

<ul>
 <li>A common use of JSON is to exchange data to/from a web server.</li>
<br/>
 <li>When receiving data from a web server, the data is always a string.</li>
<br/>
 <li>Parse the data with JSON.parse(), and the data becomes a javascript object.</li>
</ul>

<b>Example to understand it more clearly is given below:</b>

```javascript

const jsonString = `{"name":"JSON","age":30,"mobileNumber":1234567890}`;

const parsedData = JSON.parse(jsonString);

console.log(parsedData);

```
<div style="border:1px solid white;padding:10px;border-radius:15px;box-shadow:0 0 3px 3px">
Exceptions:- Date and functions are not allowed in JSON. If we need to include a date or function, add it as a string. We can convert it back into a date object or function later.
</div>

<h1>JSON.stringify()</h1>

<ul>
 <li>A common use of JSON is to exchange data to/from a web server.</li>
<br/>
 <li>When sending data to a web server, the data has to be string.</li>
<br/>
 <li>Convert a JavaScript object into a string with JSON.stringify()</li>
</ul>

<b>Example to understand it more clearly is given below:</b>

```javascript

const jsonString = {"name":"JSON","age":30,"mobileNumber":1234567890};

const stringedData = JSON.stringify(jsonString);

console.log(stringedData);

```
