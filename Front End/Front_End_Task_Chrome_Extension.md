# Front End Task: Chrome Extension

You can submit the solution in any of the following ways:

- A private or public repo
- An unpacked ctx/zip file of extension
- A public blog describing the process
- A small video of browser and extension

---

Design and Create a chrome extension,

- On click of browser icon, loads a panel on the side.
- On click of the browser icon, the panel and all data/state inside will vanish.
- It will have vertical menu (just like a ant design pro dashboard) which will open different tabs.
- You can navigate to different tabs on panel.
- Each tab will have a different form to add/edit/remove a very minimal todo list.
- The states on different panel tab should persist.
- The last tab will be a `export` tab where you can export all todo data from different panel tabs on console on click of a button.
- You are free to use any library/framework/tool, though React, Redux/Mobx is priority.

# Reference:

Here is a reference of our upcoming **automatio.co extension**. You can copy the design from this.

![](https://paper-attachments.dropbox.com/s_BB1362FF5C4EDA5375FF05D9FCE8B4F079B7C45B9A489D7A1C5ADFC3BC405DD1_1560335713380_image.png)

# Restrictions:

- It cannot be a popup.html
- It cannot be a iframe
- It must execute the panel on the current page.
- The panel must be above all elements (think z-index) on the current page.
