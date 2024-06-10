jamesdanielmarrsritchey: How do you create a TABLE element in HTML?

GitHub Copilot: To create a TABLE element in HTML, you use the `<table>` tag. Inside this tag, you can use the `<tr>` tag to create rows, and the `<td>` tag to create cells within those rows. Here's a basic example:

```html
<table>
  <tr>
    <td>Row 1, Cell 1</td>
    <td>Row 1, Cell 2</td>
  </tr>
  <tr>
    <td>Row 2, Cell 1</td>
    <td>Row 2, Cell 2</td>
  </tr>
</table>
```

This will create a table with 2 rows and 2 columns. The text inside the `<td>` tags is the content of the cells.

jamesdanielmarrsritchey: How do you add a heading to a TABLE element in HTML?

GitHub Copilot: To add a heading to a TABLE element in HTML, you use the `<th>` tag. This tag is used within a `<tr>` tag, similar to the `<td>` tag. Here's an example:

```html
<table>
  <tr>
    <th>Heading 1</th>
    <th>Heading 2</th>
  </tr>
  <tr>
    <td>Row 1, Cell 1</td>
    <td>Row 1, Cell 2</td>
  </tr>
  <tr>
    <td>Row 2, Cell 1</td>
    <td>Row 2, Cell 2</td>
  </tr>
</table>
```

In this example, the first row of the table contains the headings "Heading 1" and "Heading 2". The `<th>` tag makes the text bold and centered by default.

jamesdanielmarrsritchey: How can you add a border to a TABLE element in HTML?

GitHub Copilot: To add a border to a TABLE element in HTML, you can use the CSS `border` property. Here's an example:

```html
<style>
  table, th, td {
    border: 1px solid black;
  }
</style>

<table>
  <tr>
    <th>Heading 1</th>
    <th>Heading 2</th>
  </tr>
  <tr>
    <td>Row 1, Cell 1</td>
    <td>Row 1, Cell 2</td>
  </tr>
  <tr>
    <td>Row 2, Cell 1</td>
    <td>Row 2, Cell 2</td>
  </tr>
</table>
```

In this example, the `border: 1px solid black;` line adds a border to the table and all of its cells. The border will be 1 pixel wide, solid, and black. You can adjust these values to change the appearance of the border.

jamesdanielmarrsritchey: How can you align the content within the cells of a TABLE element in HTML?

GitHub Copilot: To align the content within the cells of a TABLE element in HTML, you can use the CSS `text-align` property for horizontal alignment and `vertical-align` property for vertical alignment. Here's an example:

```html
<style>
  th, td {
    text-align: center; /* Horizontal alignment */
    vertical-align: middle; /* Vertical alignment */
  }
</style>

<table>
  <tr>
    <th>Heading 1</th>
    <th>Heading 2</th>
  </tr>
  <tr>
    <td>Row 1, Cell 1</td>
    <td>Row 1, Cell 2</td>
  </tr>
  <tr>
    <td>Row 2, Cell 1</td>
    <td>Row 2, Cell 2</td>
  </tr>
</table>
```

In this example, the `text-align: center;` line centers the text horizontally within the cells, and the `vertical-align: middle;` line centers the text vertically. You can adjust these values to change the alignment.