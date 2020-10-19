Performing a search
You can perform a volumes search by sending an HTTP GET request to the following URI:
 Volumes Working Docs 
This request has a single required parameter:
•	q - Search for volumes that contain this text string. There are special keywords you can specify in the search terms to search in particular fields, such as: 
o	`intitle`: Returns results where the text following this keyword is found in the title.
o	`inauthor`: Returns results where the text following this keyword is found in the author.
o	`inpublisher`: Returns results where the text following this keyword is found in the publisher.
o	subject: Returns results where the text following this keyword is listed in the category list of the volume.
o	`isbn`: Returns results where the text following this keyword is the ISBN number.
o	`lccn`: Returns results where the text following this keyword is the Library of Congress Control Number.
o	`oclc`: Returns results where the text following this keyword is the Online Computer Library Center number.
•	Example:
GET
https://www.googleapis.com/books/v1/volumes?q=flowers+inauthor:keyes&key=yourAPIKey
If the request succeeds, the server responds with a 200 OK HTTP status code and the volume results
Optional query parameters
In addition to the standard query parameters, you can use the following query parameters when performing a volumes search.
Download Format
You use the download parameter to restrict the returned results to volumes that have an available download format of `epub` by setting the to the value `epub`.
The following example searches for books with an epub download available:
GET
https://www.googleapis.com/books/v1/volumes?q=pride+prejudice&download=epub&key=yourAPIKey
Filtering
You can use the filter parameter to restrict the returned results further by setting it the to one of the following values:
•	`partial` - Returns results where at least parts of the text are previewable.
•	`full` - Only returns results where all of the text is viewable.
•	`free-ebooks` - Only returns results that are free Google eBooks.
•	`paid-ebooks` - Only returns results that are Google eBooks with a price.
•	`ebooks` - Only returns results that are Google eBooks, paid or free. Examples of non-eBooks would be publisher content that is available in limited preview and not for sale, or magazines.
Pagination
You can paginate the volumes list by specifying two values in the parameters for the request:
•	`startIndex` - The position in the collection at which to start. The index of the first item is 0.
•	`maxResults` - The maximum number of results to return. The default is 10, and the maximum allowable value is 40.
Print Type
You can use the `printType` parameter to restrict the returned results to a specific print or publication type by setting it to one of the following values:
•	`all` - Does not restrict by print type (default).
•	`books` - Returns only results that are books.
•	`magazines` - Returns results that are magazines.
 
What is EJS?
What is the "E" for? "Embedded?" Could be. How about "Effective," "Elegant," or just "Easy"? EJS is a simple templating language that lets you generate HTML markup with plain JavaScript. No religiousness about how to organize things. No reinvention of iteration and control-flow. It's just plain JavaScript.
Options
•	`cache` Compiled functions are cached, requires filename
•	`filename` Used by cache to key caches, and for includes
•	`root` Set project root for includes with an absolute path (e.g, /file.ejs). Can be array to try to resolve include from multiple directories.
•	`views` An array of paths to use when resolving includes with relative paths.
•	`context` Function execution context
•	`compileDebug` When false no debug instrumentation is compiled
•	`client` Returns standalone compiled function
•	`delimiter`
•	`openDelimiter`
•	`closeDelimiter` '/li>
•	`debug` Outputs generated function body
•	`strict` When set to `true`, generated function is in strict mode
•	_with Whether or not to use with() {} constructs. If false then the locals will be stored in the `locals` object. (Implies `--strict`)
•	`localsName` Name to use for the object storing local variables when not using with Defaults to locals
•	`rmWhitespace` Remove all safe-to-remove whitespace, including leading and trailing whitespace. It also enables a safer version of -%> line slurping for all scriptlet tags (it does not strip new lines of tags in the middle of a line).
•	`escape` The escaping function used with <%= construct. It is used in rendering and is `.toString`()ed in the generation of client functions. (By default escapes XML).
•	`outputFunctionName` Set to a string (e.g., 'echo' or 'print') for a function to print output inside scriptlet tags.
•	`async` When true, EJS will use an async function for rendering. (Depends on async/await support in the JS runtime.
Tags
•	`<%` 'Scriptlet' tag, for control-flow, no output
•	`<%_` ‘Whitespace Slurping’ Scriptlet tag, strips all whitespace before it
•	`<%=` Outputs the value into the template (HTML escaped)
•	`<%-` Outputs the unescaped value into the template
•	`<%#` Comment tag, no execution, no output
•	`<%%` Outputs a literal '<%'
•	`%>` Plain ending tag
•	`-%>` Trim-mode ('newline slurp') tag, trims following newline
•	`_%>` ‘Whitespace Slurping’ ending tag, removes all whitespace after it

