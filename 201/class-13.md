## Readings: Local Storage

### 8/19/22: Our reading today is based on local storage. 
---

1. Why would a developer use local storage for a web application?

- Object stored in cache. Key/value pair, key is the name. Typically value is an object. Storage local only to specific browser and computer. 
- Storing information locally on a user's computer is a powerful strategy for a developer who is creating something for the Web.
- HTTP as main transport layer of the Web is thaat it is stateless. This means that when you use an app and then close it, its state will be reset the next time you open it. 
- If you close an app on your desktop and re-open it, its most recent state is restored. 
- This is why, as a developer, you need to store the state of your interface somewhere. 
- You would keep a key on the user's computer and read it out when the user returns. 
- The classic way to do this is by using a cookie. A cookie is a text file hosted on the user's computer and connected to the domain that your website runs on. You can store information in them, read them out and delete them. This is a rather dated solution. 
- Using local storage in modern browsers is simple. You modify the `localStorage` object in JS. You can do this directly or use the `setItem()` and `getItem()` method - this is cleaner. 
- `localStorage.setItem('favoriteflavor','vanilla');`
- If you read out the favoriteflavor key, you will get back “vanilla”: <br>
`var taste = localStorage.getItem('favoriteflavor');`
`// -> "vanilla"`
- To remove the item, you use removeItem() method: <br>
`localStorage.removeItem('favoriteflavor');`
`var taste = localStorage.getItem('favoriteflavor');`
`// -> null`
- You can also use `sessionStorage` instead of `localStorage` if you want the data to be maintained only until the browser window closes.

2. What information should not be stored in local storage?
- You should not store sensitive user information in local storage. 
- Any information that you would not share publicly.

3. Local storage can store what type of data? How would you convert it to that type before storing?

- One shortcoming of local storage is that you can only store strings in the different keys. This means that when you have an object, it will not be stored the right way. 
- `var car = {};` <br>
`car.wheels = 4;` <br>
`car.doors = 2;` <br>
`car.sound = 'vroom';` <br>
`car.name = 'Lightning McQueen';` <br>
`console.log( car );` <br>
`localStorage.setItem( 'car', car );` <br> 
`console.log( localStorage.getItem( 'car' ) );` 
- Trying this out in the console shows that the data is stored as `[object Object]` and not the real object information. 
- You can work around this by using the native `JSON.stringify()` and `JSON.parse()`.
- `setItem():` Add key and value to localStorage
- `getItem():` This is how you get items from localStorage
- `removeItem():` Remove an item by key from localStorage
- `clear():` Clear all localStorage
- `key():` Passed a number to retrieve the key of a localStorage

[Back to main page](README.md)