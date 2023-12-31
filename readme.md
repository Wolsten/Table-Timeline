# Table Timeline

4th Dec 2023

## Introduction

Table timeline is a simple Javascript program that takes a correctly structured HTML table and converts it into a graphical timeline and formatted with a custom stylesheet.

A timeline table should be structured as a simple table composed of TABLE, TR and TD tags as follows:

## Installation

The main files you need are the javascript module `table-timeline.js` and the css file `style.css`.

Link the css file in the head of your page:

`<link rel="stylesheet" href="style.css">`

and add the script tag at the end of the page body:

`<script src="table-timeline.js"></script>`

## Usage

```
<table class="timeline-table" title="timeline name">

    [<style>
            table {
                --colour-category-1: hsl(123, 70%, 57%);
                --colour-category-2: hsl(194, 60%, 60%);
                --colour-category-3: hsl(221, 80%, 70%);
                --colour-category-4: hsl(300, 63%, 46%);
                --colour-category-5: hsl(60, 90%, 70%);
                --colour-category-6: hsl(0, 85%, 47%); 
            }
    </style>]

    <tr>
        <td>Event name</td>
        <td>Start</td>
        <td>End date</td>
        <td>Category</td>
        <td>Summary</td>
        <td>Citations</td>
    </tr>
</table>
```

Timeline tables are identified with the class `timeline-table` and named via their `title` attribute. They also have an optional `styles` tag which can be used to override the colours for each category of event. If not provided a set of default colours will be used. These are specified in the `style.css` file.

Dates can be formatted in a number of ways:

-   Year, _e.g. 2023_
-   UTC date, _e.g. 2023-12-25_
-   Gregorian calendar, _e.g. 100BC and 2023BC_
-   Common era, e.g. _e.g. 100BCE and 2023BE_
-   Geologic, _e.g. 4.5bya, where units can be bya, mya and tya_

Gregorian, common era and geologic indicators are case-insensitive.

Each timeline can mix date types for different events. Ongoing events are specified by setting their end date to the word **date** or **-**. Events can just have a start time (i.e. instants), in which case the end date should be left blank.

There is also a node script for converting an Excel spreadsheet table into the equivalent HTML page to display as a graphical timeline. This does not support custom style attributes at present.

## MIT Licence

Copyright (c) 2023 Stephen John Davison

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
