# JS Challenge: `sortBy`
You can submit the solution in any of the following ways:

- A private or public repo
- A secret GitHub gist
- A public blog describing the process. 
----------
# Sort Array By Reference Position

There are three arrays, the first two is the input and last one is output. 

The task:
Sort the "**source**" based on the order of the elements inside "**reference**", so the end result looks like the "**output**".


    const reference = [
      ".currency-name",
      "#currencies .market-cap",
      ".price",
      ".volume",
      ".circulating-supply",
      ".percent-change"
    ];
    
    const source = [
      ".currency-name",
      ".currency-name",
      "#currencies .market-cap",
      ".price",
      ".circulating-supply",
      ".volume",
      ".percent-change"
    ];
    
    // preview of how it should look
    const output = [
      ".currency-name",
      ".currency-name",
      "#currencies .market-cap",
      ".price",
      ".volume",
      ".circulating-supply",
      ".percent-change"
    ];
    
    // write the following function
    function sortBy(source, reference){
      // return output
    }

