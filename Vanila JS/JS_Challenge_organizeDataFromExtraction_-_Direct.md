# JS Challenge: `organizeDataFromExtraction` - Direct
You can submit the solution in any of the following ways:

- A private or public repo
- A secret GitHub gist
- A public blog describing the process. 
----------

Write a function which takes a input and options.


    function organizeDataFromExtraction(input, {leaf = false, fill = true}){
      return output;
    }

Sample input data: [Sample JSON](sample.json)

Read the nested object and organize the data so it looks similar to below. 

    [
      {
        "Currency Name.innerText": "Bitcoin",
        "Currency Link.href": "https://coinmarketcap.com/currencies/bitcoin/",
        "Market Cap.innerText": "$147,214,625,533",
        "Price.innerText": "$8,289.85",
        "Volumn.innerText": "$19,144,814,369",
        "Supply.innerText": "17,758,412 BTC",
        "Percent Change.innerText": "2.21%"
      },{
        "Currency Name.innerText": "Ethereum",
        "Currency Link.href": "https://coinmarketcap.com/currencies/ethereum/",
        "Market Cap.innerText": "$27,260,018,680",
        "Price.innerText": "$256.00",
        "Volumn.innerText": "$8,633,995,209",
        "Supply.innerText": "106,485,536 ETH",
        "Percent Change.innerText": "-0.72%"
      }
    ]

The sample input data can change so you should not hardcode the keys.

Also, not all object will have **leaf/field/content** data. If the object does not have any of them, then it should not generate the key/value for that object.

Look at the following change, the object is empty or does not have content/field/leaf.

![](https://paper-attachments.dropbox.com/s_21C06C45EAEB1DC5D52E875ACB02456928356E09945F671EC5F15A7E270755C1_1560588008806_image.png)


Considering the above change, If **fill** is **false**, the output might look like below. Notice it does not have **Currency Link** for Bitcoin.

    [
      {
        "Currency Name.innerText": "Bitcoin",
        "Market Cap.innerText": "$147,214,625,533",
        "Price.innerText": "$8,289.85",
        "Volumn.innerText": "$19,144,814,369",
        "Supply.innerText": "17,758,412 BTC",
        "Percent Change.innerText": "2.21%"
      },{
        "Currency Name.innerText": "Ethereum",
        "Currency Link.href": "https://coinmarketcap.com/currencies/ethereum/",
        "Market Cap.innerText": "$27,260,018,680",
        "Price.innerText": "$256.00",
        "Volumn.innerText": "$8,633,995,209",
        "Supply.innerText": "106,485,536 ETH",
        "Percent Change.innerText": "-0.72%"
      }
    ]

If **leaf** if **true**, the output should not have the leaf like **innerText** **href** etc. 

    [
      {
        "Currency Name": "Bitcoin",
        "Currency Link": "https://coinmarketcap.com/currencies/bitcoin/",
        "Market Cap": "$147,214,625,533",
        "Price": "$8,289.85",
        "Volumn": "$19,144,814,369",
        "Supply": "17,758,412 BTC",
        "Percent Change": "2.21%"
      },{
        "Currency Name": "Ethereum",
        "Currency Link": "https://coinmarketcap.com/currencies/ethereum/",
        "Market Cap": "$27,260,018,680",
        "Price": "$256.00",
        "Volumn": "$8,633,995,209",
        "Supply": "106,485,536 ETH",
        "Percent Change": "-0.72%"
      }
    ]

**fill** and **leaf** options should respect each other. 

# Notes:
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

