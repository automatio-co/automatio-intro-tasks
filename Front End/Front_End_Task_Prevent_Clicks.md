# Front End Task: Prevent Clicks

You can submit the solution in any of the following ways:

- A private or public repo
- GitHub gist
- A public blog describing the process.
- A deployed version
- A small video of browser console just like the demo video below

---

Create two functions,
`**addBlocker()**`

- Should block all clicks on the page. Nothing should be clickable anymore.
- Should print the current mouse position on viewport, and the current element under the mouse on click.

`**removeBlocker()**`

- Should remove the blocker created by addBlocker(), everything should be clickable as before adding the blocker.

The two functions should work on **any website** including,]

- [dev.to](http://dev.to/)
- [producthunt.com](http://producthunt.com/)

Here is a video preview of what should be done.

Link: [https://youtu.be/ZkVPheXNqoc](https://youtu.be/ZkVPheXNqoc)

# Restrictions:

1. You **cannot** use the following functions or methods.

- stopImmediatePropagation
- stopPropagation
- preventDefault
- elementFromPoint
- appendChild
- pointerEvents

2. The solution must be done in vanila JS or jQuery. No other libraries are allowed.
