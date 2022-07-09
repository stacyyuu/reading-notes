## Javascript and HTML

### 7/9/22: Our reading today is based on JavaScript basics and an introduction to HTML. This is important for our lab where we are learning to create a webpage that allows our user to make an input and receive a message in response to the input. 

---


## JavaScript Basics
1. Compose a short poem describing how HTTP sends data between computers.
- Web address is typed into browser
- Browser goes to DNS server and finds real address of server where website lives
- Browser sends HTTP request message to server, asking to send a copy of website to client
- Message and all other data sent between client and server is sent across internet connection using TCP/IP
- If server approves client's request, server sends client "200 OK" message
- This means, "Of course you can look at the website! Here it is,"
- Server starts sending website's files to browser as series of small chunks called **data packets**.
- Browser assembles small chunks into complete webpage and displays it to you

2. Describe how HTML, CSS, and JS files are “parsed” in the browser.
- Once browser receives first chunk of data, it can begin parsing the information received. 
- **Parsing** is the step the browser takes to turn data it received over the network into **DOM** and **CSSOM**, which is used by the renderer to paint a page to the screen. 
- Parsing occures from top to bottom. 
- Before anything is rendered to screen, HTML, CSS, and JavaScript need to be parsed. 

3. How can you find images to add to a Website?
- You can use **Google Images** to search for something suitable. 
- When you find an image, click on it to enlarge it, then right-click to save the image. 
- It is a good idea to save the image in a safe place and also have a copy of the image web address.
- Most images on the web are copyrighted, but Google Images provides a tool to help reduce violations. 
- Google Images provides a license filter. To access click on the *Tools* button, then *Usage Rights*. You can choose the option *Creative Commons licenses* that allows you to use images without "stealing".

4. How do you create a String vs a Number in JavaScript?
- String: `let myName = "Stacy";`
- Number: `let myAge = 28;`

5. What is a Variable and why are they important in JavaScript?
- **Variables**: Lets values be stored in containers. 
- Declared with `let` keyword, followed by the name of the variable. 
- Semicolon `;` is where the statement ends. It is only required when you need to separate statements on a single line. However, people believe it's good practice to have semicolons at the end of each statement. 
- You can name a variable nearly anything, with some restrictions. 
- Variables may hold values that are different data types: **string**, **number**, **boolean**, **array**, **object**.

<br>

## Introduction to HTML

1. What is an HTML attribute?
- **Attributes**: Contain extra information about the element that won't appear in content. 
- Ex. `<p class>`, `class` attribute is an identifying name used to target the element with style information. 
- An attribute should have a space between it and the element name, attribute name followed by equal sign, and an attribute value wrapped with opening and closing quote marks. 

2. Describe the Anatomy of an HTMl element.
- **Opening Tag**: Consists of name of element wrapped in opening and closing angle brackets. This opening tag marks where the element begins or starts to take effect `<p>`. 
- **Content**: What the element contains `<p> content of element </p>`. 
- **Closing Tag**: Same as opening tag, except it includes a forward slash before element name `</p>`.

3. What is the Difference between <article> and <section> element tags?
- `<article>`: Encloses block of related content that makes sense on its own without rest of the page. 
- `<section>`: Similar to `<article>`, but more for grouping together a single part of the page that constitutes one single piece of functionality or theme. It is best practice to begin each section with a heading. 
- Can break `<article>`s into different `<section>`s, or `<section>`s up in different `<article>`s. 

4. What Elements does a “typical” website include?
- **Header**: `<header>`
- **Navigation Bar**: `<nav>`
- **Main Content**: `<main>`. With varioius content subsections represented by `<article>`, `<section>`, and `<div>` elements. 
- **Sidebar**: `<aside>`; often placed inside `<main>`. 
- **Footer**: `<footer>`.

5. How does metadata influence Search Engine Optimization?
- The description is used in search engine result pages. 

6. How is the <meta> HTML tag used when specifying metadata?
- `<meta>` tag goes inside the `<head>` element. 
- Metadata is data that describes data. 

<br>

## Miscellaneous
**How to start designing a website**:
1. What is the first step to designing a Website?
- Establish your goals and vision. 

2. What is the most important question to answer when designing a Website?
- "What exactly do I want to accomplish?"

**Semantics**:
1. Why should you use an `<h1>` element over a `<span>` element to display a top level heading?
- `<h1>` gives the text it is wrapped around, "a top level heading on your page."
- `<span>` would not give it the semantic value, even if you could make it look like a top level heading. 

2. What are the benefits of using semantic tags in our HTML?
- Lets us know what type of data will be in the content. 
- Makes code more organized. 

**What is JavaScript?**
1. Describe 2 things that require JavaScript in the Browser?
- Interactive maps
- Shopping carts
- Animated graphics 
- Timely updates

2. How can you add JavaScript to an HTML document?
- Using `<script>` tag and added into the `<head>` tag of the HTML.

## Things I want to know more about:
- Parsing: understanding exactly how the process works. 