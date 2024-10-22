# Front End Task: Partial Data Extraction

You can submit the solution in any of the following ways:

- A private or public repo
- GitHub gist
- A public blog describing the process
- A deployed version
- A small video of browser console

---

We have setup a simple demo page ([click here](https://entrptaher.github.io/playground-partial-extraction/) to open).

Your task will be to write a function called **extractData()** to extract the title and subtitle from the blue boxes into an array.

![Click to get a bigger picture](https://paper-attachments.dropbox.com/s_D3D02C284C1AD135CFEC5696FDC4188E7AAA83967FDBE177459B1828A81FA612_1559326267824_image.png)

There are three main noticeable points:

- Each box is randomly generated, sometimes it has title (class **.title**), sometimes subtitle (class **.subtitle**).
- Each box might have different tag, ie: span, section, div, article.
- You cannot use `boxes` element directly. `document.getElementById('boxes')` or `document.querySelector('#boxes')` is not allowed.

Regardless of the format,
- We need to extract the data using **document.querySelector** or some other way. You are free to use any library or tool.
- It should work with slight or no change if I change the selectors and the text inside title/subtitle, or the order of them.
- You cannot grab the data from the script tag. That is for demo purpose only.
- We should be able to run your code on the browsers console and see the result in the array like below.

## Most Important Rule

You cannot use `boxes` element directly. `document.getElementById('boxes')` or `document.querySelector('#boxes')` is not allowed. 

The following and similar variants are allowed,
- `document.querySelector('.title')`
- `document.querySelector('.subtitle')`

These following and any related variants are forbidden,
- `document.querySelector('body > div:nth-child(1)')`
- `document.querySelector('#boxes')`
- `boxes.children`

You also cannot query for title/subtitle and find parentNode till you reach `boxes`. 
```
const boxes = document.querySelector('.title').parentNode
```

Any solution that maps over the childnodes of boxes is not accepted. Such as below
```js
boxes.children.map(element=>{
  element.querySelector('.title'); 
  element.querySelector('.subtitle')
}
```

You have to figure out the parent element for `.title` and `.subtitle` in some other way. 

# Demo
Here’s how I did it for demo purpose.

![Click to get a bigger picture](https://paper-attachments.dropbox.com/s_D3D02C284C1AD135CFEC5696FDC4188E7AAA83967FDBE177459B1828A81FA612_1559326064685_image.png)

You can share me the code in a GitHub gist or any code sharing site, write a blog about it, or show a small video. All I need to know about your DOM related skills. 😄

Good Luck!
