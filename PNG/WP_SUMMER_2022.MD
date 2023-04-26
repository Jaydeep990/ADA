# WP SUMMER 2022

## Q.1

### (A) Give full name of following acronym. 1) WWW 2) CSS 3) AJAX - 03

```TXT
1) WWW stands for World Wide Web.
2) CSS stands for Cascading Style Sheets.
3) AJAX stands for Asynchronous JavaScript and XML.
```

### (B) Explain different design issue at the time of designing an effective website. - 04

```TXT
There are several design issues that need to be considered while designing an effective website. Here are some of the important ones:

1. User Experience (UX): The website design should focus on providing a great user experience. This includes easy navigation, clear calls to action, a consistent layout, and fast loading times.

2. Mobile Responsiveness: With the increasing use of mobile devices, it is important to design websites that are mobile-responsive. This means that the website should be easily accessible and readable on all screen sizes, including smartphones and tablets.

3. Accessibility: The website should be designed to be accessible to all users, including those with disabilities. This includes using alternative text for images, providing transcripts for videos, and ensuring that the website is easily navigable using assistive technology.

4. Branding: The website should reflect the branding of the business or organization. This includes the use of the company's logo, color scheme, and typography.

5. Content: The website should be designed with the content in mind. This includes ensuring that the layout and design are optimized for the content, and that the content is easily readable and scannable.

6. Search Engine Optimization (SEO): The website should be designed with SEO in mind. This includes optimizing the website for search engines, using relevant keywords in the content, and ensuring that the website is easily crawlable by search engine bots.

7. Security: The website should be designed to be secure. This includes using secure protocols for data transmission, implementing SSL certificates, and ensuring that user data is protected.

8. Performance: The website should be designed to be fast and performant. This includes optimizing images and other media files, minimizing HTTP requests, and using a content delivery network (CDN) to improve load times.

By considering these design issues while designing a website, one can create a website that is effective, efficient, and provides a great user experience.
```

### (C) What is HTTP? Explain how browser and server communicate using HTTP request and response. - 07

```TXT
HTTP, or Hypertext Transfer Protocol, is a protocol used for transferring data over the internet. It is the foundation of data communication for the World Wide Web. When you browse the web, your browser sends an HTTP request to a server, which then responds with an HTTP response.

The process of browser and server communication using HTTP can be explained as follows:

1. The client (usually a web browser) sends an HTTP request to the server. The request contains a URL (Uniform Resource Locator) that specifies the web page or resource that the client wants to access.

2. The server receives the request and processes it. It determines which resource the client is requesting and retrieves the corresponding data from the server's file system or database.

3. The server generates an HTTP response message, which includes the requested data and some metadata about the response, such as the response status code and content type.

4. The server sends the HTTP response message back to the client.

5. The client receives the HTTP response message and processes it. It displays the requested resource (such as a web page) in the browser window, based on the content type specified in the response message.

Throughout this process, HTTP is used to transfer the data between the client and the server. The HTTP protocol specifies the format of the messages that are exchanged between the client and server, including the structure of the requests and responses, the headers that provide additional information about the messages, and the status codes that indicate the success or failure of the request.

HTTP is a stateless protocol, which means that each request and response is independent of any other requests or responses that came before it. This allows the protocol to be efficient and scalable, but it also means that applications must handle session state and other forms of state management explicitly.
```

## Q.2

### (A) Explain ordered list and unordered list in HTML. - 03

```TXT
In HTML, lists are used to group related items together. There are two types of lists: ordered lists and unordered lists.

1. Ordered Lists: 

An ordered list is a list in which the items are numbered sequentially. The numbering of the items is done automatically by the browser. In HTML, ordered lists are created using the <ol> tag. Each item in the list is represented by the <li> (list item) tag. Here is an example of an ordered list in HTML:
```

```HTML
<ol>
<li>Item 1</li>
<li>Item 2</li>
<li>Item 3</li>
</ol>

<!-- The above code will create an ordered list with three items, numbered 1, 2, and 3. -->
```

```TXT
2. Unordered Lists:

An unordered list is a list in which the items are bulleted or marked with some other symbol. In HTML, unordered lists are created using the <ul> tag. Like ordered lists, each item in the list is represented by the <li> tag. Here is an example of an unordered list in HTML:
```

```HTML
<ul>
<li>Item 1</li>
<li>Item 2</li>
<li>Item 3</li>
</ul>

<!-- The above code will create an unordered list with three items, each of which is marked with a bullet point. -->
```

```TXT
In summary, ordered lists are used to represent items in a sequential order, while unordered lists are used to represent items in a non-sequential order. Both types of lists are useful for organizing information and presenting it in a structured way on a web page.
```

### (B) Explain following html tags with proper example. 1. \<img> 2. \<frameset> - 04

```TXT
1. <img> Tag:

The <img> tag is used in HTML to embed an image on a web page. This tag does not have a closing tag as it is a self-closing tag. The image can be a JPEG, PNG, GIF, or any other format that is supported by web browsers. Here's an example of how to use the <img> tag:
```

```HTML
<img src="image.jpg" alt="A beautiful image">
```

```TXT
In the above example, the "src" attribute specifies the URL or file path of the image to be displayed. The "alt" attribute provides alternative text for the image, which is displayed if the image cannot be loaded or read by the browser. 
```

```TXT
2. <frameset> Tag:

The <frameset> tag is used to define a set of frames in an HTML document. Frames allow multiple HTML documents to be displayed in a single browser window, each with its own scrollbars and other features. The <frameset> tag is used to define the layout of the frames, and the <frame> tag is used to specify the individual frames. Here's an example of how to use the <frameset> tag:
```

```HTML
<!DOCTYPE html>
<html>
<head>
 <title>My Frameset Example</title>
</head>
<frameset cols="25%,75%">
 <frame src="menu.html" name="menu">
 <frame src="content.html" name="content">
</frameset>
</html>
```

```TXT
In the above example, the <frameset> tag is used to define a two-column layout with a menu frame on the left and a content frame on the right. The "cols" attribute specifies the width of each column as a percentage of the total window width. The <frame> tag is used to define the content of each frame, with the "src" attribute specifying the URL or file path of the HTML document to be displayed. The "name" attribute provides a unique name for each frame, which can be used to target links and other elements to a specific frame.

Note that frames are not widely used in modern web design due to accessibility issues and other concerns. Instead, web developers typically use other layout techniques such as CSS and responsive design to achieve similar effects.
```

### (C) What is rowspan and colspan used in HTML? Give examples. - 07

```TXT
Both rowspan and colspan are attributes used in HTML to merge cells in a table.

1. rowspan: 

The rowspan attribute is used to merge cells vertically (i.e., across rows) in a table. The value of the rowspan attribute specifies the number of rows that a cell should span. Here is an example of how to use the rowspan attribute:
```

```HTML
<table>
  <tr>
    <td rowspan="2">Merged cell</td>
    <td>Cell 1</td>
  </tr>
  <tr>
    <td>Cell 2</td>
  </tr>
</table>
```

```TXT
In the above example, the first cell in the first row has a rowspan of 2, which means that it spans two rows. As a result, the first cell in the second row is merged with the first cell in the first row to create a single merged cell that spans two rows.
```

``` TXT
2. colspan: 

The colspan attribute is used to merge cells horizontally (i.e., across columns) in a table. The value of the colspan attribute specifies the number of columns that a cell should span. Here is an example of how to use the colspan attribute:
```

```HTML
<table>
  <tr>
    <td>Cell 1</td>
    <td colspan="2">Merged cell</td>
  </tr>
  <tr>
    <td>Cell 2</td>
    <td>Cell 3</td>
    <td>Cell 4</td>
  </tr>
</table>
```

```TXT
In the above example, the second cell in the first row has a colspan of 2, which means that it spans two columns. As a result, the second cell in the first row is merged with the third cell in the first row to create a single merged cell that spans two columns.

Both rowspan and colspan attributes are useful for creating complex tables with merged cells, which can be used to display data in a more organized and understandable way.
```

### (C) What do you mean by “class” and “id” in CSS? Explain with Example. - 07

```TXT
In CSS, classes and IDs are used to select and style specific HTML elements. 

1. Class in CSS:

A class is a way to define a set of style rules that can be applied to one or more HTML elements. To define a class in CSS, we use the period (.) followed by the name of the class. Here is an example:
```

```HTML
<style>
  .my-class {
    color: red;
    font-size: 18px;
  }
</style>
```

```TXT
In the above example, we define a class called "my-class" which applies the style rules of red text color and 18px font size to any HTML element that uses this class.

To apply this class to an HTML element, we add the class name as a value of the "class" attribute. For example:
```

```HTML
<p class="my-class">This text is red and 18px.</p>
```

```TXT
2. ID in CSS:

An ID is a way to select a specific HTML element and apply style rules to it. To define an ID in CSS, we use the pound (#) symbol followed by the ID name. Here is an example:
```

```HTML
<style>
  #my-id {
    background-color: blue;
    color: white;
    padding: 10px;
  }
</style>
```

```TXT
In the above example, we define an ID called "my-id" which applies the style rules of blue background color, white text color, and 10px padding to the HTML element that uses this ID.

To apply this ID to an HTML element, we add the ID name as a value of the "id" attribute. For example:
```

```HTML
<div id="my-id">This div has a blue background, white text, and 10px padding.</div>
```

```TXT
Note that IDs should be unique within an HTML document, while classes can be used multiple times on different elements.
```

## Q.3

### (A) Explain HTML media tags. - 03

```TXT
HTML media tags are used to embed various types of media content, such as audio, video, images, and other multimedia files, into an HTML document. There are several media tags available in HTML, including:

1. <img> tag:

The <img> tag is used to embed images into an HTML document. The tag has a "src" attribute that specifies the URL of the image file to be displayed. Here is an example:
```

```HTML
<img src="image.jpg" alt="Example image">
```

```TXT
In the above example, we use the <img> tag to embed an image with a source file of "image.jpg" and an alternate text of "Example image".
```

```TXT
2. <audio> tag:

The <audio> tag is used to embed audio content into an HTML document. The tag has several attributes such as "src", "controls", and "autoplay" that specify the audio source file, control options, and autoplay settings. Here is an example:
```

```HTML
<audio src="music.mp3" controls autoplay></audio>
```

```TXT
In the above example, we use the <audio> tag to embed an audio file with a source file of "music.mp3", with controls and autoplay enabled.
```

```TXT
3. <video> tag:

The <video> tag is used to embed video content into an HTML document. The tag has several attributes such as "src", "controls", "autoplay", and "poster" that specify the video source file, control options, autoplay settings, and poster image. Here is an example:
```

```HTML
<video src="video.mp4" controls autoplay poster="poster.jpg"></video>
```

```TXT
In the above example, we use the <video> tag to embed a video file with a source file of "video.mp4", with controls and autoplay enabled, and a poster image of "poster.jpg".
```

### (B) What is positioning in CSS? - 04

```TXT
In CSS, positioning refers to the process of placing HTML elements on a web page, either absolutely or relatively, according to their position within the page's HTML structure.

There are four different types of positioning in CSS:

1. Static: This is the default position value of an HTML element. The element is positioned in the normal flow of the document, and cannot be moved using top, bottom, left or right properties.

2. Relative: This position value allows an element to be positioned relative to its normal position within the HTML structure, by using the top, bottom, left, or right properties. The element will still take up space in its original position, and other content will flow around it.

3. Absolute: This position value allows an element to be positioned relative to its nearest positioned ancestor, such as a parent element with a position value other than static. The element is removed from the normal flow of the document, and other content will flow into the space previously occupied by the element.

4. Fixed: This position value is similar to absolute positioning, but the element is positioned relative to the browser window, rather than its nearest positioned ancestor. The element will remain in the same position even when the user scrolls the page.

To use positioning in CSS, we can set the position property of an HTML element to one of the above values, and then use the top, bottom, left, or right properties to adjust its position within the web page.
```

```HTML
<div style="position: relative; top: 50px; left: 50px;">
  This div is positioned 50 pixels down and 50 pixels to the right from its normal position.
</div>
```

```TXT
In the above example, we set the position of the <div> element to relative, and then use the top and left properties to move it 50 pixels down and to the right from its normal position.
```

### (C) What is document object model? Explain any two objects with example. - 07

```TXT
The Document Object Model (DOM) is a programming interface for web documents that allows HTML and XML documents to be manipulated as objects. With the DOM, web developers can create, modify, and delete HTML elements and their attributes on a web page. The DOM represents the document as nodes and objects, which can be manipulated with a scripting language like JavaScript.

Here are two examples of objects in the DOM:

1. The Element Object:

The Element object represents an HTML element on a web page. It has many properties and methods that can be used to manipulate the element's attributes and content. For example, we can use the Element's "style" property to change the element's CSS styles:
```

```HTML
<!DOCTYPE html>
<html>
  <head>
    <style>
      #myDiv {
        background-color: yellow;
      }
    </style>
  </head>
  <body>
    <div id="myDiv">Hello, World!</div>
    <script>
      var myDiv = document.getElementById("myDiv");
      myDiv.style.color = "red";
    </script>
  </body>
</html>
```

```TXT
In the above example, we use the getElementById() method to select the "myDiv" element, and then change its text color to red using the "style" property.
```

```TXT
2. The Document Object:

The Document object represents the entire HTML document on a web page, and contains properties and methods that can be used to manipulate the document as a whole. For example, we can use the Document's "title" property to change the title of the document:
```

```HTML
<!DOCTYPE html>
<html>
  <head>
    <title>My Web Page</title>
  </head>
  <body>
    <script>
      document.title = "New Title";
    </script>
  </body>
</html>
```

```TXT
In the above example, we use the Document's "title" property to change the title of the document from "My Web Page" to "New Title".

These are just two examples of the many objects available in the Document Object Model, which allow web developers to manipulate and interact with HTML documents using a scripting language.
```
