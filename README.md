# css-layout-snippets
This is a helpful CSS layout snippets 

## Make Center 
#### Using Flexbox layout
```
.parent-element {
  display: flex; 
  align-items: center; 
  justify-content: center; 
  
  height: 100vh; 
  width: 100vw; 
}
```
#### Using Grid layout
```
.parent-element {
  display: grid; 
  place-items: cente;r 
  
  height: 100vh; 
  width: 100vw; 
}
```




## Sidebar with min-max width 
HTML
```
<parent>
  <sidebar>sidebar</sidebar>
  <conent>main content of page</conent>
</parent>
```

CSS
```
.parent-element {
  display: grid;
  grid-template-column: minmax(200px, 25%) 1fr; 
}

```



## Stack Left and Right Columns
First & Third column : auto width based on content
Second column : take the available space
```
.parent-element {
  display: grid;
  grid-template-column: auto 1fr auto;
}
```


## Classic Grid layout
HTML
```
<div class="body-element">
  <div class="header"></div>
  <div class="left-side"></div>
  <div class="main-content"></div>
  <div class="right-side"></div>
  <div class="footer"></div>
</div>
```

CSS
```
.body-element {
  display: grid;
  grid-template: auto 1fr auto / auto 1fr auto;
}

.header {
  grid-column: 1/4; 
}

.left-side {
  grid-column: 1/2; 
}


.main-content {
  grid-column: 2/3; 
}


.right-side {
  grid-column: 3/4; 
}


.footer {
  grid-column: 1/4; 
}
```

## 12-column layout
HTML
```
<div class="parent-element">
  <div class="header"></div>
  <div class="left"></div>
  <div class="main"></div>
  <div class="footer"></div>
</div>
```

CSS 
```
.parent-element {
  gisplay : grid;
  grid-template-columns: repeat(12, 1fr)
}

.header {
  grid-column:1/13;
}

.left {
  grid-column:1/4;
}

.main {
  grid-column:4/13;
}

.footer {
  grid-column: 1/13;
}
```

## Card List Layout 
```
.parent-element {
  gisplay: grid;
  grid-template-columns: repeat (auto-fill, minmax (200px, 1fr));
}
```
OR 
```
.parent-element {
  gisplay: grid;
  grid-template-columns: repeat (auto-fit, minmax (200px, 1fr));
}
```

