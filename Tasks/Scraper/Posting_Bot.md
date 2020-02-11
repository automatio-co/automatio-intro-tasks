# Posting Bot

**First make sure the code is well commented, tested and have a nice documentation** and then you can submit the solution in any of the following ways:

- A private repo (add `taher@vanila.io` as collaborator)
- A secret GitHub gist
- A public blog describing the process
- A small video of browser and terminal console

---
Create a simple puppeteer script which will do following and report us via websocket in every step. It should be waiting for the instruction from third party. WebSocket is strongly recommended for this task.

Notes:

- There will be a minimal frontend with login form for the bot. How the UI or data structure should look is totally upto you. 
- A table that lists link to last post so we know which post or comment was made last time. 
- The bot will be hosted on a different server. 
- We must ensure multiple people can login and post at same time (we can use a single react state per tab in our browser. No Passport/JWT needed.)

Interaction:

- open browser, load http://demo.realworld.io, 
    - wait for the login details
    - submit and finish login
    - wait for next instruction.
- Whenever we give it a title, tag, description etc, 
    - it should publish it
    - give us the link to the post
    - wait for next instruction.
- If we give it a link and a comment, 
    - it should go to that page
    - post a comment.
    - wait for next instruction.
