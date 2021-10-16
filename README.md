# Welcome to loadit!
Load github projects in html table for personal website use.

## Requirements:
- jquery (works on 3.5.1 version)
- loadit-js/ folder

## Process:

- add loadit-js/ folder to your project

- import necessary javascript files: 

```html
<!-- jquery library CDN -->
<script src="https://ajax.googleapis.com/ajax/libs/jquery/3.5.1/jquery.min.js"></script>

<!-- loadit libraries -->
<script type="text/javascript" src="loadit-js/app.js"></script>
<script type="text/javascript" src="loadit-js/projects-content.js"></script>
<script type="text/javascript" src="loadit-js/projects-pagination.js"></script>
<script type="text/javascript" src="loadit-js/projects-table.js"></script>
<script type="text/javascript" src="loadit-js/utils.js"></script>
<script type="text/javascript" src="loadit-js/variables.js"></script>
```

- add next struct to your html file (you can change html to include classes, check our [website example](https://bakincode.github.io/) and respective [source code](https://github.com/bakincode/bakincode.github.io)):

```html
<div id="projects">
    <!-- buttons for different ordering methods-->
    <button onclick="loadProjects('created')" type="button">CREATION DATE</button> 
    <button onclick="loadProjects('full_name')" type="button">NAME</button>
    <button onclick="loadProjects('updated')" type="button">UPDATE DATE</button>
                
    <!-- projects tables -->
    <table id="projectsTable">
        <!-- head -->
        <thead>
            <tr>
                <th style="width: 30%">Name</th>
                <th style="width: 15%">Created</th>
                <th style="width: 15%">Last update</th>
                <th style="width: 20%">Language (most used)</th>
                <th style="width: 20%"></th>
            </tr>
        </thead>

        <!-- content -->
        <tbody id="projectTableContent">

        </tbody>
    </table>
        
    <ul id="pagination"></ul>
</div>
```

- add function loadProjects('created') to your onload body tag: 
```html
<body onload="loadProjects('created');"></body>
```

- set variables like your GitHub username on [loadit-js/variables.js](https://github.com/bakincode/loadit/blob/main/loadit-js/variables.js):
```javascript
//  only variables in this js file can be changed

//  set your github username here
const githubUsername = 'yourGithubUsername'

//  --------------------------------------------------------------
//  --------------------------------------------------------------
//  --------------------------------------------------------------

//  CUSTOMIZE CLASSES AND TEXT OF TABLE AND PAGINATION:


//  --------------------------------------------------------------
//  HTML TAGS TABLE
//  tags <tr> and <td> of table with content:

//  <tr> tag
var classForTrTagOfHtmlTable = ""

//  <td> tag 
var classForTdTagOfHtmlTable = ""
//  --------------------------------------------------------------

//  --------------------------------------------------------------
//  PAGINATION:
//  These two variables refer to classes for pagination item and link, and you can change them.

//  <li> tag
var classForPaginationItem = ""

//  <a>  tag
var classForPaginationLink = ""
//  --------------------------------------------------------------

//  set text, icon for download link column
const downloadItem = 'download'

//  number of projects per project table
const maxProjectsPerPage = 6

//  --------------------------------------------------------------
//  --------------------------------------------------------------
//  --------------------------------------------------------------
```

## Contributing:
Contributions are welcome, contact us at bakincode@gmail.com.
