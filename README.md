HTML Element Processor
Overview
The HTML Element Processor is a JavaScript library that dynamically processes custom HTML tags (e.g., <p3>, <li2>, <section4>) and replaces them with multiple standard HTML elements based on attributes like text, changeclass, changeid, etc. It supports elements like paragraphs, lists, links, sections, images, audio, video, inputs, and more.
Features

Converts custom tags (e.g., <p3>) into multiple standard HTML elements (e.g., three <p> tags).
Supports attributes for dynamic class, ID, text, and other properties using JSON-parsed arrays.
Provides warnings for invalid attributes or missing text to aid debugging.
SEO-friendly warnings for inappropriate use of text attributes on container elements.

Installation
The library is available via CDN for easy integration into your web projects. No local installation is required.
CDN Link
<script src="https://cdn.jsdelivr.net/gh/yourusername/html-element-processor@1.0.0/processor.min.js"></script>

Note: Replace yourusername with your actual GitHub username and update the version tag (e.g., 1.0.0) as needed.
Usage

Include the CDN link in your HTML file:<script src="https://cdn.jsdelivr.net/gh/yourusername/html-element-processor@1.0.0/processor.min.js"></script>


Use custom tags in your HTML with appropriate attributes. Example:<p3 text='["First paragraph", "Second paragraph", "Third paragraph"]' class="para" changeclass='["class1", "class2", "class3"]'></p3>


The script automatically processes the custom tags when the page loads, replacing them with standard HTML elements.

Example
<!DOCTYPE html>
<html>
<head>
  <title>HTML Element Processor Demo</title>
</head>
<body>
  <p2 text='["Hello", "World"]' class="text" changeid='["id1", "id2"]'></p2>
  <li3 text='["Item 1", "Item 2", "Item 3"]' changetitle='["Title 1", "Title 2", "Title 3"]'></li3>
  <script src="https://cdn.jsdelivr.net/gh/yourusername/html-element-processor@1.0.0/processor.min.js"></script>
</body>
</html>

This will generate:
<p class="text" id="id1">Hello</p>
<p class="text" id="id2">World</p>
<li title="Title 1">Item 1</li>
<li title="Title 2">Item 2</li>
<li title="Title 3">Item 3</li>

Supported Tags

<pN>: Paragraphs
<liN>: List items
<aN>: Links
<sectionN>, <divN>, <articleN>, <navN>, <ulN>, <headerN>, <footerN>, <mainN>, <asideN>: Container elements
<imgN>: Images
<audioN>: Audio elements
<videoN>: Video elements
<inputN>: Input fields
<optionN>: Select options

Replace N with the desired number of elements (e.g., <p3> for three paragraphs).
Attributes

text: JSON array of text content (e.g., ["Text 1", "Text 2"]).
changeclass: JSON array of class names (e.g., ["class1", "class2"]).
changeid: JSON array of IDs (e.g., ["id1", "id2"]).
changetitle: JSON array of title attributes (for <li>, <a>, <input>, <option>).
changehref: JSON array of href attributes (for <a>).
src, alt: JSON arrays for <img>, <audio>, <video>.
changetype, changename, changevalue, changeplaceholder: JSON arrays for <input> and <option>.

Terms of Use

This library is provided for use via the CDN link only.
Unauthorized copying, modification, or redistribution of the source code is prohibited.
Please respect the license terms included in the repository.

License
This project is licensed under the MIT License with additional restrictions on copying. See the LICENSE file in the repository for details.
Contributing
This project is not open for contributions at this time. For suggestions or issues, please contact the repository owner.
Contact
For support, please open an issue on the GitHub repository: yourusername/html-element-processor.
