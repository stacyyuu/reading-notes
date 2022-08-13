## Readings: Audio, Video, Images

### 7/9/22: Our reading today is based on reading, video and audio content, gris, and responsive images. 
---

## Video and Audio Content

1. Explain how the ability to use video and audio on the web has evolved since the early 2000s.
-   Videos and audio were made possibly by proprietary plugin-based technologies like Flash and Silverlight. Both of these had security and accessibility issues. 
- `<video>` and `<audio>` elements and the availability of JS APIs for controlling them is what is favored now. 

2. Describe the use of the src and controls attributes in the `<video>` element.
- `<video>` element allows you to embed a video very easily. 
-   `<video src="rabbit320.webm" controls>`<br>
  `<p>Your browser doesn't support HTML video. Here is a <a href="rabbit320.`<br>`webm">link to the video</a> instead.</p>`<br>
`</video>`
- Features of note are:
- `src`, in the same way as for the `<img>` element, the source attribute contains a path to the video you want embed. It works exactly the same way. 
- `controls`, users must be able to control video and audio playback, especially critical for people who have epilepsy. You must either use the controls attribute to include the browser's own control interface, or build your interface using the appropriate JS API. At min, the interface must include a way to start and stop the media, and to adjust the volume. 

3. Why is it important to have fallback content inside the `<video>` element?
- The paragraph inside the `<video>` tags is called **fallback content** - this will be displayed if the browser accesing the page doesn't support the `<video>` element, allowing us to provide a fallback for older browsers. This can be anything you like, for example, a direct link to the video. 
- Other features include:
- `autoplay`, makes the audio or video start playing right away, while the rest of the page is loading. Usually not advised because it can be annoying for users. 
- `loop`, makes the audio or video loop plays. This can also be annoying. 
- `width` and `height`.
- `poster`, the URL of an image which will be displayed before the video is played. Intended to be used for splash screen or advertising screen. 

4. Write a very short story where `<audio>` and `<video>` are characters.
- `<audio>` element works just like the `<video>` element, with a few small differences as outlined below. 
- `<audio controls>`<br>
  `<source src="viper.mp3" type="audio/mp3">`<br>
  `<source src="viper.ogg" type="audio/ogg">`<br>
  `<p>Your browser doesn't support this audio file. Here is a <a href="viper.`<br>`mp3">link to the audio</a> instead.</p>`<br>
`</audio>`
- This takes up less space than a video player, as there is no visual component - you just need to display controls to play audio. 
- Other differences:
- It doesn't support the `width/height` attributes. 
- It also doesn't support the `poster` attribute. 
- Other than this, `<audio>` supports all the same features as `<video>`.

## A Complete Guide to Grid 

1. How does Grid layout differ from Flex?
- Grid Layout is a two-dimensional grid-based layout system that, compared to any web layout system of the past, completely changes the way we design user interface. 
- Flexbox has a one-directional flow which has different use cases and they work together quite well. 
- Grid was created to solve layout problems we've all been hacking our way around for making websites. 
- `grid`, generates a block-level grid.
- `inline-grid`, generates an inline-level grid.
- `.container {
  display: grid | inline-grid;
}`

2. Grid container, grid item, and grid line are a few important terms to understand when using Grid. Please describe these terms in a few sentences.
- **Container**: The element on which display: grid is applied. It's the direct parent of all the grid items. 
- **Item**: The children (direct decendants) of the grid container.
- **Line**: The dividing lines that make up the structure of the grid. They can be either vertical (column grid lines) or horizontal (row grid lines) and reside on either side of a row or column. 
- **Cell**: The pace between two adjacent row and two adjacent column grid lines. It's a single "unit" of the grid. 
- **Track**: The space between two adjacent grid lines. You can think of them as the columns or rows of the grid. 
- **Area**: The total space surrounded by four grid lines. A grid area may be composed of any number of grid cells. 

## Responsive Images

1. Besides making a site visually appealing across different screen sizes, why should developers make images responsive?
- This helps to improve performance across different devices. Reponsive images are just one part of responsive design. 
- Displaying a large image on a screen significantly smaller than the size it was meant for can waste bandwidth, in particular, mobile users don't want to waste bandwidth by downloading a large image intended for desktop users. 

2. Define the following `<img>` attributes srcset and sizes. Write an example of how they are used.
- `<img srcset="elva-fairy-480w.jpg 480w,`<br>
             `elva-fairy-800w.jpg 800w"`<br>
     `sizes="(max-width: 600px) 480px,`<br>
           ` 800px"`<br>
    ` src="elva-fairy-800w.jpg">`<br>
    `alt="Elva dressed as a fairy">`
- `srcset`, defines the set of images we will allow the browser to choose between, and what size each image is. Each set of image information is separated from the previous one by a comma. For each one we write:
- 1. an **image filename** (elva-fairy-480w.jpg).
- 2. A space.
- 3. The image's **intrinsic width in pixels** (480w) - note that this uses the `w` unit, not `px` as you might expect. The image's intrinsic size is it's real size, which can be found by inspecting the image file on your computer. 

- `sizes`, defines a set of media conditions (ex. screen width) and indicates what image size would be best to choose, when certain media conditions are true - these are the hints we talked about earlier. Before each comma, we write: 
- 1. A **media condition** (max-width: 600px) - describes a possible state that the screen can be in. 
- 2. A space.
- 3. The **width of the slot** the image will fill when the media condition is true (480px).

3. How is srcset more helpful for responsive images than CSS or JavaScript?
- When the browser starts to load a page, it starts to download (preload) any images before the main parser has started to load and interpret the page's CSS and JS. That mechanism is useful in general for reducing page load times, but it's not helpful for responsive images. 
- For example, you couldn't load the `<img>` element, then detect the viewport width with JavaScript, and then dynamically change the source image to a smaller one if desired. By then, the original image would already have been loaded, and you would load the small image as well, which is even worse in responsive image terms. That's why it is needed to implement solutions such as `srcset`. 

[Back to main page](README.md)