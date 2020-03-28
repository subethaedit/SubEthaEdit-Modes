[Documentation][ModeExample]:
## Web Preview: _WebPreview.js_

The file called `WebPreview.js` is located in the mode's `Resources` folder. It is used to generate HTML from plain text which will be displayed in the Web Preview Panel. Typical use cases are processing markup languages like Markdown, Textile, etc. The `webPreview(text)` takes the document text as an input parameter and is expected to return the processed HTML.


### <a name="ExampleFile"></a>Example File:

```js
// This function escapes the document and wraps it into <pre></pre> tags
function webPreview(text) {
	const escaped = text.replace(/&/g, "&amp;")
         .replace(/</g, "&lt;")
         .replace(/>/g, "&gt;")
         .replace(/"/g, "&quot;")
         .replace(/'/g, "&#039;");
	return `<pre>${escaped}</pre>`
}
```



<!-- Referenced Paths -->
[ModeExample]: .. "SubEthaEdit 4 Example Mode Documentation"
