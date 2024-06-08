jamesdanielmarrsritchey: How is a PDF file structured internally?

GitHub Copilot: A PDF file is structured in the following way:

1. **Header**: The first line of a PDF file is a header which identifies the version of the PDF specification to which the file conforms. For example, `%PDF-1.7` indicates the file is formatted according to the PDF 1.7 specification.

2. **Body**: The body of a PDF file contains the objects that make up the content of the document. These objects can include text, images, annotations, form fields, and more. Each object is numbered and can be referenced by other objects.

3. **Cross-Reference Table**: The cross-reference table gives the byte offset of each object from the start of the file. This allows a PDF reader to quickly find and load objects without reading the entire file.

4. **Trailer**: The trailer of a PDF file contains information needed to read the cross-reference table and the location of the root object of the document's object hierarchy.

5. **EOF Marker**: The end of a PDF file is marked by `%%EOF`.

It's worth noting that PDF files can also be incrementally updated. In this case, changes are appended to the end of the file, along with a new cross-reference table and trailer that apply only to the updates. This allows changes to be made without rewriting the entire file.