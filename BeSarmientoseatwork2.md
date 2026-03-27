# Seatwork #2 - Getting to know CSS Position and z-index.
### This seatwork will ask you to implement the different CSS position on a given code.
### short link to this .md file is: https://bit.ly/4c61P9K
#### Resources (also found in Khub week 5)
- [4 Minute Youtube Video on CSS Position](https://www.youtube.com/watch?v=YEmdHbQBCSQ)
- [CSS Position Tutorial](https://roycan.github.io/CssPositioningZIndexLab/)

### Instructions: 
1. This is individual submission in khub, but you can work with a partner.  When you submit in khub please place both your names in the submission bin.
2. Guided Activity (30 minutes), please follow what is being required.  

    - Make a copy of this .md file to your Q4 repository and name it as **SectionLNseatwork2.md** example **9LiCruzSeatwork2.md**. Place it in your q4 repository vscode local computer. Committing frequently to your Github repository.  
    - Copy the code below and paste it inside a new file (name it as SectionLNseatwork2.html). Place this file in the same location where the .md file is saved. 
    - Change the content values of the meta tags to your names for author/s and the date today for revised.
    - Please do the following tasks that will ask you to reposition HTML elements then answer the guided question for each task on the .md file. Commit changes to the .md file and to the .html file as well.
    **- This seatwork is worth 20pts and should be submitted by the end of the period** The link to [KHub submission bin](https://khub.mc.pshs.edu.ph/mod/assign/view.php?id=15481).
      - Submit the links to your .md file and .html file.

```html
<!DOCTYPE html>
<html>
<head>
  <meta name="author" content="<your names>" />
  <meta name="revised" content="<date today>" />
  <style>
    body { font-family: Arial, sans-serif; }
    .header, .footer {
      background: lightblue;
      padding: 10px;
    }
    .footer {
       opacity: 0.5;
    }
    .sidebar {
      background: lightgreen;
      width: 150px;
      height: 200px;
    }
    .content {
      background: lightyellow;
      width: 300px;
      height: 200px;
    }    
  </style>
</head>
<body>
  <div class="header">Header</div>
  <div class="sidebar">Sidebar</div>
  <div class="content">Main Content</div>
  <div class="footer">Footer</div>
</body>
</html>
```
### Step 1 (Static vs Relative):

- Add in css ```position: relative; top: 20px; left: 20px;``` to .sidebar.

- Guided Question: What changed compared to the default static positioning? Try to give different values to top and left or you can change it to bottom, right.
- The position of the sidebar changed relative to its original position.

### Step 2 (Fixed):

- Add in css ```position: fixed; bottom: 0; width: 100%;``` to .footer.

- Guided Question: What happens when you scroll the page? Why does the footer behave differently from position relative?
- The footer's position stays completely fixed to the bottom of the screen. To me, it doesn't seem to change its position at all relative to the other parts of the webpage as it also overlaps with them if I scroll high enough.

### Step 3 (Absolute):

- Add in css ```position: absolute; top: 66px; left: 200px;``` to .content.

- Guided Question: What is the effect of position: absolute on an element? How is it different from fixed?
- Fixed positioning makes an element stuck to the screen even as you scroll, as for absolute positioning, it gives the element with it the freedom to move within the space of the higher div that it is part of. 

### Step 4 : (Absolute)

- Add in html ```<div class="notice">Notice!</div>``` and include the css below:

```css
.notice {
    position: absolute;
    top: 60px;
    left: 400px;
    background: orange;
    padding: 10px;
    z-index: 2;
}
```

- Give .content a z-index: 1.

- Guided Question: Why does the notice appear on top of the content? What happens if you swap the z‑index values?
- Notice appears on top of the content because its z-index is higher than content's. If I were to swap their z-index values, then content would appear on top of notice and almost cover it fully.

- Challenge: 
    * What changes that you have to do on the code that will position .notice box on the top right corner of the .content box? Please write the code on paper as well (both html and css on the part of .notice and .content).
    -  .notice {
    position: absolute;
    top: 30px;
    left: 500px;
    background: orange;
    padding: 10px;
    z-index: 2;
    }
    * Try to change the position of .content to relative then to fixed. What do you observed each time?
    - For relative, the content dropped down to
    * What do you observe on about the effect of z-index on .notice and .content boxes?

3. Please answer the following reflection questions (15 minutes)

    a. Could you summarize the differences between the CSS position values (static, relative, absolute, fixed)? 
    - Static position is the default position of the element when added into the code. Relative position moves the element relative to its static position. Absolute position moves the element anywhere in the space of the higher div group (parent element) that it is part of. Fixed position makes the element stuck at a certain part of the screen so that as you scroll, it doesn't move.

    b. How does absolute positioning depend on its parent element?
    - Absolute positioning depends on its parent element as that parent element defines the space in which the object with absolute positioning can move in.

    c. How do you differentiate sticky from fixed (you can research on sticky)?
    - Sticky is a position value like static positioning until a certain scroll threshold wherein if that threshold is exceeded, the sticky position element will start behaving like a fixed position element. 

    d. If you were designing a webpage for a school event, how might you use positioning to highlight important information? Please give concrete examples.
    - I would only use some position values to highlight certain important information. For example, I would use
      - Fixed positioning to show the credits of the creators of the webpage.
      - Static positioning to center the schedule/primer of the event.
      - Absolute positioning to add in additional reminders for the safety of the event.
