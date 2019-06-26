# Scraper: Extract Data from Playground

You can submit the solution in any of the following ways:

- A private or public repo
- A secret GitHub gist
- A public blog describing the process
- A small video of browser and terminal console

---

I have a scraping playground here: http://scraper-playground.surge.sh/

**Rule 1:** I need the following for specific number of users in a single array.

- Name
- ID
- Address
- Phone
- Email

**Rule 2:** If any details is missing, then it should be left as an empty string **“”**.

The structure should be similar to below,

```json
[
  {
    "name": "Danny Mendez",
    "address": "5a984736-a698-50e5-a85b-5ef3ca8ae333",
    "id": "",
    "phone": "",
    "email": ""
  },
  {
    "name": "Charlie Russell",
    "address": "716 Tejom Road",
    "id": "1fc5a4d6-8b77-5a47-aae8-27f82b7681ff",
    "phone": "",
    "email": ""
  }
]
```

**Rule 3:** The scraper must not refresh the page. The data is randomized on each refresh.

There are two parts of this and you need to do each part separately. You can use code from one part into another part and put them on same repository if you want.

## Part 1: Create a Function for Browser’s Console

The function **extractPeople()** will be executed on the browser console. It should handle clicking elements, waiting for modal and pagination.

I should be able to get as many people as I want to extract. **limit** is the number of people I want to extract.

```js
function extractPeople(limit) {
  return array;
}
```

## Part 2: Create a Package for NodeJS

Create a private nodeJS package **extract-people** which will use headless chrome using puppeteer to execute the data on the page.

It should handle clicking elements, modal and pagination.

I should be able to run the following in the console,

```bash
    cd extract-people
    node index.js --limit=100
```

It should include tests which can be run using,

```bash
    cd extract-people
    npm run test
```

**Note:**

- You **cannot publish** the package to any kind of public npm registry, because this is a specific use case.
