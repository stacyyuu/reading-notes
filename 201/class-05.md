## HTML Links, CSS Layout, & JS Functions

### 7/22/22: Our reading today is based on images, color, & text. 

---

## HTML Media: Using Images in HTML

1. What is a real world use case for the `alt` attribute being used in a website?
- `alt` stands for Alternative Text. Its value is meant to be a textual description of the image, for use in situations where the image cannot be seen/displayed or connection is taking a long time. 
- It is useful for someone who is visually impaired and using a screen reader to read the web out to them. 

2. How can you improve accessibility of images in an HTML document?
- Provide thorough information in the alt text, prioritizing the most important information in the beginning. Make sure that the length of the alt text is concise. 
- It may be helpful to add a description of th image in HTML. 
- It is important to make images accessible for screen readers, speech input software, speech-enabled websites, mobile users, and SEO. 


3. Provide an example of when the `figure` element would be useful in an HTML document.
- Using `<figure>` tag is used to semantically organize content of images, videos, audios, charts or tables, or block of codes in the HTML document. 
- Using `<figcaption>` tag allows you to provide a caption to the describe the content of the `<figure>` content.
- Figure is a container for contents and figcaption provides a caption for it. 

4. Describe the difference between a gif image and an svg image, pretend you are explaining to an elder in your community.
- **Gif**: Graphics Interchange Format `image/gif`. Good choice for simple images and animations. Supported: Chrome, Edge, Firefox, IE, Opera, Safari. 
- **SVG**: Scalable Vector Graphics `image/svg+xml`. Vector image format; ideal for user interface elements, icons, diagrams, etc. that must be drawn accurately at different sizes. Supported: Chrome, Edge, Firefox, IE, Opera, Safari. 
- GIF, just like other image formats, are not resolution-independent, and will therefore look pixelated when scaled up or viewed on higher resolutions. 
- SVG is scalable and resolution-independent, and will look crisp clear on any screen resolution. 

5. What image type would you use to display a screenshot on your website and why?
- Photographs: Fare well with lossy compression. **WebP or JPEG**.
- Icons: For smaller images, use lossless format to avoid loss of detail in a size-constrained image. **SVG, Lossless WebP, or PNG**. 
- Screenshots: Lossless format to keep quality. Especially important if there's any text in your screenshot. **Lossless WebP or PNG; JPEG if compression artifacts aren't a concern like text**.
- Diagrams, drawings, and charts: Any image that can be represented using vector graphics, **SVG** is best choice. 

## Learn CSS: Using Color in CSS & Styling HTML Text Elements

1. Describe the difference between foreground and background colors of an HTML element, pretend you are talking to someone with no technical knowledge.
- **Foreground** defines the color of the HTML element's content. It changes the color of the actual text.
- **Background-color** defines the element's background color. It changes the background color of the text or content. 

2. Your friend asks you to give his colorless blog website a touch up. How would you use color to give his blog some character?
- Change the webpage background color by adding background-color to the body property. 
- Add text color by adding color to the header and parts of the body texts. 

3. What should you consider when choosing fonts for an HTML document?
- There are only a certain number of fonts that are generally available across all systems and can therefore be used without much worry. These are called **web safe fonts**. These are available on most used operating systems such as Windows, macOS, common Linux distributions, Android, and iOS. 
- The list of web safe fonts will change as operating systems evolve. 
- Arial, Courier New, Georgia, Times New Roman, Trebuchet MS, Verdana. 

4. What do `font-size`, `font-weight`, and `font-style` do to HTML text elements?
- `font-size` changes the size of the font. The default size is `16px` or `1rem`. You can use either `px` or `rem` to alter the size. 
- `font-weight` sets how bold the text is. This has many values available. `-light, -normal, -bold, -extrabold, -black`, etc.
- `font-style` turns italics on or off. `normal` sets text to normal font. `italic` sets text to italic. `oblique` sets text to simulated version of an italic font, created by slanting the normal version. This is used when italic is not available. 

5. Describe two ways you could add spacing around the characters displayed in an h1 element.
- `letter-spacing` and `word spacing`. 

- `text-align` aligns within its containing content box. `left, right, center, justify`. Justify makes the text spread out, varying the gaps in between the words so that all lines of text are the same width. 

[Back to main page](README.md)