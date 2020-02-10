# Back End Task: Stripe Connect

You can submit the solution in any of the following ways:

- A private or public repo
- GitHub gist
- A public blog describing the process.
- A deployed version
- A small video of playground or postman

---

**Create a dummy bookstore app** where author can connect their own stripe connect account and sell their book. The bookstores stripe account should get 20% as processing fee and 80% shall go to the authors stripe account.

# Submission:

Either of following,

- A **short video** using loom.com, 
    - of setting up stripe account as an author.
    - buying a book as a reader.
    - watching the profit as an author.
- A **private github/bitbucket** repo (so other applicants don’t copy and use it for themselves). You must write down how to start this project and provide some screenshots in the readme.md file.
- A **deployed version** of the project, so we can test it out. 
    - Provide the username/password for the author and dummy information for the reader.
    - If it’s just an API, provide the JSON payload needed to get the right output.
## Rules:
- Author’s can signup and login to see their stats, create book, connect their stripe.
- Author can set their own store on bookstores.com (or localhost in this case).
- Author can connect their own stripe account to the store.
- Author can see how many books they have sold and how much profit they made using the api/frontend.
- Reader doesn’t need an account. 
- Reader can buy book from author’s provided link using their credit card. A simple success message is shown on correct purchase.
![](https://paper-attachments.dropbox.com/s_C32F9B0204AA5D8CC4851FA70F213E0A7724B40269D514087AD7C2CD5A4672ED_1575102079955_image.png)

# Stack:

**Frontend:** 

- The front-end is not a priority for this test. Most of the tasks can be easily done using the API. Even a simply one line text and a button is okay just to make sure it works. *But if you design a nice looking frontend, that’d be a plus towards the evaluation.*
- Use anything, react + redux/mobx is preferred.

**Backend (JavaScript):**

- JavaScript (NodeJS) or TypeScript
- ExpressJS
- GraphQL ([Prisma](https://www.prisma.io/), [Hasura](https://hasura.io/), [Postgraphile](https://www.graphile.org/postgraphile/))
- MongoDB/MySQL/PostgreSQL
# Hints:

**Links:**

- Read the [documentation for Stripe Connect](https://stripe.com/docs/connect/standard-accounts) - standard accounts.
- [An old (but good) post](https://adamjstevenson.com/stripe/2017/10/20/building-a-marketplace-using-stripe-connect-examples.html) about stripe connect.
- [Example stripe connect marketplace project](https://stripe-marketplace-demo.herokuapp.com/) using Rails.

**Getting Test Account:**
You can create a test account for stripe and turn the test mode on. When you go to the **Apps** page, you should be able to turn on the Connect integration.

![](https://paper-attachments.dropbox.com/s_C32F9B0204AA5D8CC4851FA70F213E0A7724B40269D514087AD7C2CD5A4672ED_1575101258594_image.png)
