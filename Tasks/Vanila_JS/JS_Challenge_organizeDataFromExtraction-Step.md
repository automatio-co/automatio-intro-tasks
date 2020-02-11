# Organize Data from Extraction

You can submit the solution in any of the following ways:

- A private repo (add `taher@vanila.io` as collaborator)
- A secret GitHub gist
- A public blog describing the process.

---

# Rearrange Array of Object with Key

Given this source: [Sample JSON](sample.json)

The output should be similar to this format,

```json
[
  {
    "Currency Name.innerText": "Bitcoin",
    "Currency Link.href": "https://coinmarketcap.com/currencies/bitcoin/",
    "Market Cap.innerText": "$147,214,625,533"
  },
  {
    "Currency Name.innerText": "LiteCoin",
    "Currency Link.href": "https://coinmarketcap.com/currencies/bitcoin/",
    "Market Cap.innerText": "$147,214,625,533"
  },
  {
    "Currency Name.innerText": "Dashcoin",
    "Currency Link.href": "https://coinmarketcap.com/currencies/bitcoin/",
    "Market Cap.innerText": "$147,214,625,533"
  }
]
```

Write a function **reArrangeWithFieldLeaf** that takes array of arrays and return the converted data.

![](https://paper-attachments.dropbox.com/s_A93CEE5B394E4BA540D89B6FF099C7207447A9EF7CD1A0433A7D2E17899928FB_1560531008649_image.png)

Some objects might not have all key (like content, elem, field etc.), in that case it should not create any keys/fields for that object.

Look at the **input** of the problem below called **Refill Missing Keys** to understand this.

# Refill Missing Keys

Consider the following input

```json
[
  {
    "Currency Name.innerText": "Bitcoin",
    "Currency Link.href": "https://coinmarketcap.com/currencies/bitcoin/",
    "Market Cap.innerText": "$147,214,625,533"
  },
  {
    "Currency Name.innerText": "LiteCoin",
    "Currency Link.href": "https://coinmarketcap.com/currencies/bitcoin/"
  },
  {
    "Currency Name.innerText": "Dashcoin",
    "Market Cap.innerText": "$147,214,625,533"
  }
]
```

It should look like this,

```json
[
  {
    "Currency Name.innerText": "Bitcoin",
    "Currency Link.href": "https://coinmarketcap.com/currencies/bitcoin/",
    "Market Cap.innerText": "$147,214,625,533"
  },
  {
    "Currency Name.innerText": "LiteCoin",
    "Currency Link.href": "https://coinmarketcap.com/currencies/bitcoin/",
    "Market Cap.innerText": ""
  },
  {
    "Currency Name.innerText": "Dashcoin",
    "Currency Link.href": "",
    "Market Cap.innerText": "$147,214,625,533"
  }
]
```

Write a function **refillMissingKeys** that takes the input array and produces the output.

# reArrangeWithField

The same problem as **reArrangeWithFieldLeaf**, but it should output the following instead,

```json
[
  {
    "Currency Name": "Bitcoin",
    "Currency Link": "https://coinmarketcap.com/currencies/bitcoin/",
    "Market Cap": "$147,214,625,533"
  },
  {
    "Currency Name": "LiteCoin",
    "Currency Link": "https://coinmarketcap.com/currencies/bitcoin/",
    "Market Cap": "$147,214,625,533"
  },
  {
    "Currency Name": "Dashcoin",
    "Currency Link": "https://coinmarketcap.com/currencies/bitcoin/",
    "Market Cap": "$147,214,625,533"
  }
]
```

# Create `organizeDataFromExtraction`

Optimize `reArrangeWithFieldLeaf`, `reArrangeWithField` and `refillMissingKeys` and merge the solutions into one function called **organizeDataFromExtraction.**

- You can use any library
- Write some tests for every case mentioned above
- Optimize for speed/performance
- Remove as many loops as possible
- Remove duplicate functions
- Keep it modular, functions should be in different files if possible
- Make it readable
  - Explain **why** in the comments
  - Don’t write comments that we don’t need
  - If the solution is from stackoverflow/any other online source, write the link in comments

The function can look like following,

```js
function organizeDataFromExtraction(input, { leaf = false, fill = true }) {
  return output;
}
```
