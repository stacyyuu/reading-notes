# PWAs

### What are PWAs?
- What does Progressive in Progressive Web App mean?
  - They are built with modern APIs and deliver enhanced capabilities, reliability, and installability while reaching anyone, anywhere, on any device with a single codebase. 

- What are three benefits of writing a progressive web app, as opposed to a native app?
  - Capable, reliable, and installable. 

- What are two reasons to consider a native app, instead of a PWA?
  - If you are creating an app that is platform-specific. 

### App Manifests
- When a website has an app manifest, what is it able to do?
  - It tells the browser about your PWA and how it should behave when installed on the user's desktop or mobile device.
  - A typical manifest file includes app name, icons the app should use, and URL that should be opened when the app is launched, etc. 
  - It is commonly named manifest.json. 

- Name and describe how short_name and two other manifest properties are used.
  - `short_name` is used on the user's home screen, launcher, or other places where space may be limited. `name` is used when the app is installed. This represents the app name.
  - When the user installs your PWA, you can define a set of icons for the browser to use on the home screen, app launcher, task switcher, splash screen, and so on.
  - The `icons` property is an array of image objects. Each object must include `src`, `size`, and `type` of image. 
  - `id` property allows you to explicitly define the identifier used for your app. 
  - `start_url` is required and tells the browser where your app should start when it's launched and prevents the app from starting on whatever page the user was on. 
  - `background_color` used on splash screen when app is first launched on mobile. 
  - `display` is used to customize the browser UI shown. 

- How does Chrome render a PWA splash screen?
  - Chrome automatically creates the splash screen from the manifest properties, specifically: `name`, `background_color`, `icons`. 