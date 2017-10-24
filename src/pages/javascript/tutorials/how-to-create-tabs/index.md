---
title: How to Create Tabs
---
## How to Create Tabs

### Introduction
The tabs structure consists of an unordered list of tabs that have hashes corresponding to tab ids. Here you will construct a simple tab structure using `HTML`, `CSS` and `JavaScript`.

Then when you `click` on each tab, only the container with the corresponding tab id will become visible. The `click` event will be triggered by some `JavaScript`, from <a href='https://developer.mozilla.org/en-US/docs/Web/Guide/Events/Event_handlers' target='_blank' rel='nofollow'>event handlers</a> in the `HTML` markup.

#### Just Show Me The Code!
A live example can be found <a href='https://codepen.io/101Computing/pen/CgAtn' target='_blank' rel='nofollow'>here - CodePen/Tabs</a> and a full draft of the code is near the bottom.

### Step 1. The Markup

The markup, or `HTML`, provides the structure for the tab structure.

```HTML
<div id="tab1" onClick="selectTab(1);">Tab 1</div>
<div id="tab2" onClick="selectTab(2);">Tab 2</div>
<div id="tab3" onClick="selectTab(3);">Tab 3</div>
<br/>
<div id="tab1Content">
  Welcome to tab 1!
</div>
<div id="tab2Content">
  Welcome to tab 2!
</div>
<div id="tab3Content">
  Welcome to tab 3!
</div>
```
### Step 2. Style with CSS

The `CSS` provides you with different states for your tabs. Things like visibility, positioning, and hover effects.

Your style sheet should look like this:
```
#tab1, #tab2, #tab3 {
  float: left;
  padding: 5px 10px 5px 10px;
  background: #126D8D;
  color: #FFFFFF;
  margin: 0px 5px 0px 5px;
}

#tab1:hover, #tab2:hover, #tab3:hover {
  background: #0C4A60;
}

#tab1Content, #tab2Content, #tab3Content {
  width: 500px;
  height: 100px;
  padding: 20px;
  border: 1px solid #126D8D;
}

#tab1Content {
  display: block; 
}

#tab2Content, #tab3Content {
  display: none; 
}
```
### Step 3. JavaScript

Your JavaScript should look like this:

```
function selectTab(tabIndex) {
  // Hide all tabs
  document.getElementById('tab1Content').style.display = "none";
  document.getElementById('tab2Content').style.display = "none";
  document.getElementById('tab3Content').style.display = "none";

  // Show the selected tab
  document.getElementById('tab' + tabIndex + 'Content').style.display = "block";
}
```

And thats it! Now put all the code together. You should now have a functional tab structure. 

### All The Code

```html
<body>
  <style>
    #tab1, #tab2, #tab3 {
      float: left;
      padding: 5px 10px 5px 10px;
      background: #B00098;
      color: #FFFFFF;
      margin: 0px 5px 0px 5px;
    }

    #tab1:hover, #tab2:hover, #tab3:hover {
      background: #E800C9;
    }

    #tab1Content, #tab2Content, #tab3Content {
      width: 500px;
      height: 100px;
      padding: 20px;
      border: 1px solid #B00098;
    }

    #tab1Content {
      display: block; 
    }

    #tab2Content, #tab3Content {
      display: none; 
    }
  </style>
  <div id="tab1" onClick="selectTab(1);">Tab 1</div>
  <div id="tab2" onClick="selectTab(2);">Tab 2</div>
  <div id="tab3" onClick="selectTab(3);">Tab 3</div>
  <br/>
  <div id="tab1Content">
    Welcome to tab 1!
  </div>
  <div id="tab2Content">
    Welcome to tab 2!
  </div>
  <div id="tab3Content">
    Welcome to tab 3!
  </div>
  <script>
    function selectTab(tabIndex) {
      // Hide all tabs
      document.getElementById('tab1Content').style.display = "none";
      document.getElementById('tab2Content').style.display = "none";
      document.getElementById('tab3Content').style.display = "none";

      // Show the selected tab
      document.getElementById('tab' + tabIndex + 'Content').style.display = "block";
    }
  </script>
```
