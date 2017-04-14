# Extract-Directory-Name
Extract or Find a Directory from URL using PHP

```
<?php
$_SERVER['REQUEST_URI_PATH'] = parse_url($_SERVER['REQUEST_URI'], PHP_URL_PATH);
$segments = explode('/', substr($_SERVER['REQUEST_URI_PATH'], 1));
?>
```
Example:
If I wanted a different sidebar for the **blog** directory in this URL:
https://jamesnorthard.com/blog/page/2/ I would use the following code:

```
<?php
$_SERVER['REQUEST_URI_PATH'] = parse_url($_SERVER['REQUEST_URI'], PHP_URL_PATH);
$segments = explode('/', substr($_SERVER['REQUEST_URI_PATH'], 1));
if ($segments[0] == "blog"){$get_sidebar = 'blog-sidebar';}
?>
```
In this example $segments[0] would be **blog**, $segments[1] would be **page**, and $segments[2] would be **2**.
