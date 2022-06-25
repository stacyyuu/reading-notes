# HTML
**6/23/22** 
### Today, in Code 102 we learned how to write and use HTML and the importance of wireframing. 

--- 

**HTML** (HyperText Markup Language) is the code used to structure a webpage and its content. HTML consists of a series of elements where you enclose around different parts of content to make it appear, or act a certain way. Enclosing tags can make a word or image hyperlink to a different location, can italize words, can make font bigger or smaller, and so on. 

**Main parts of elements**:
- **Opening and closing tag**: <> where the element begins, </> where the element ends. 
- **Content**: What exists in between the tags, such as text. 
- **Element**: Consists of the opening and closing tag and the content. 

**Attributes**: Ex. `<p class ="editor-notes">` My cat is very grumpy `</p>`. <br> "class" is attribute name and "editor-notes" is attribute value. 

**Nesting elements**: Elements can be placed inside other elements.
<br> Ex. `<p>` My cat is `<strong>` very `</strong>` grumpy `</p>`.

**Semantics**: Refers to the *meaning* of piece of code. "What purpose or role does HTML element have?"
<br>Ex of semantics in HTML. `<article>`, `<footer>`, `<main>`, `<summary>`

| **Element**            |          **Function** |
| :---: | :---: |
| `<!DOC TYPE html>` | Required preamble. Makes sure documents behave correctly. |
| `<html></html>` | Wraps all content on entire page, root element. |
| `<head></head>` | Acts as container for all the stuff you want to include on HTML page that isn't content you are showing to viewers. Includes page description, CSS, and more. |
| `<meta charset="utf-8>` | Sets character set your document should use to UTF-8, which includes most characters from vast majority of languages. There's no reason not to set this. |
| `<title></title>` | Sets title of page, which is the title that appears in browser tab when page is loaded. |
| `<body></body>`| Contains all content you want to show to page viewers. |
| `<img src="image url" alt="image description">`| Inserts an image. With the alt attribute, you specify descriptive text for viewers who cannot see the image.  |
| `<h1></h1>`| Creates headings, contains 6 levels. |
| `<!-- HTML comment -->`| Adding comments, not visible on page. |
| `<p></p>`| Contains paragraphs. |
| `<ul></ul>`| Creates unordered list, must be placed outside <li> element. |
| `<ol></ol>`| Creates ordered list, must be placed outside <li> element. |
| `<a href="url">URL name</a>`| Creates an external link. |

<br>

# Wireframing 
**Wireframe** is a screen blueprint that is used as a visual guide representing the skeletal framework of a website before the coding process. This can be done in different ways, such as hand drawn or using tools found on the computer. Three key principles of a good wireframe includes: Clarity, confidence, simplicity.   
<br>Example of the process from design to implementation:
<br> **Sketch > Wireframe > Visual > Code**

## Steps to Wireframe
1. **Do research**: Understand who your audience is, who your competitors are, and the industry. 
2. **Prepare research for quick reference**: Create a cheatsheet with all quantitative and qualitative data to use. 
3. **Have user flow mapped out**: Have an idea of how many screens will need to be produced and the flow you expect users to follow. 
4. **Draft, don't draw. Sketch, don't illustrate**: Outline and represent features and formats. You do not illustrate in fine detail. 
<br>
- Organize content to support user goal. 
- Detail what is most prominent information, where it should go, and what the user sees first on the page. 
- What the user expects to see on certain areas of the page. 
- What buttons or touch points the user needs to complete desired actions. 
5. **Add some detail and get testing**: Add some informational details to prepare the wireframe for upgrade. 
<br> 
- Usability conventions, such as putting the navigation at the top next to your logo, having a search box on the top right, and so on.
- Simple, instructional wording for i.e. calls-to-action.
- Trust-building elements: What is needed to build user's trust and where to place these elements. 
- Tooltips to indicate any functionality that could be included in a prototype transition.
6. **Start tunung wireframes into prototypes**: Start developing high-fidelity prototypes. Well-known tools such as **Sketch** helps you do this. Once wireframes are developed in Sketch, you can import them into prototyping tool, **InVision**. This is the cross between wireframing to prototyping. 

[Back to main page](README.md)