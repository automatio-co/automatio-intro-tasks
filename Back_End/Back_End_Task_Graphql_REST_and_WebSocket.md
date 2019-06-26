# Back End Task: Graphql, REST and WebSocket

You can submit the solution in any of the following ways:

- A private or public repo
- GitHub gist
- A public blog describing the process.
- A deployed version
- A small video of playground or postman

---

Consider a big app which has lots of different ways to connect to a central database. We somehow have to provide data for different clients.

We have following structure for products array/collection,

```graphql
{
  products: [
    {
      id: String,
      transactions: [
        {
          id: String,
          quantity: Int,
          time: DateTime
        }
      ]
    }
  ];
}
```

We need a **minimal app** that can be used for all three purposes listed below. You are free to use any library, structure, services etc.

**Note**: The three part below describes **Read** of CRUD.

That means you can use any method, or mutation to create, update or delete the product and transactions. The schema and specification for those other methods are upto you.

## Part 1: REST

I can query the products with REST (POST and/or GET) api.

**Query for all products**

```
    /products
```

Expected output should be similar to:

```json
[
  {
    "id": "abc123",
    "transaction": [
      {
        "id": "abc123",
        "quantity": 123,
        "time": 1559328117100
      }
    ]
  },
  {
    "id": "abc124",
    "transaction": [
      {
        "id": "abc124",
        "quantity": 124,
        "time": 1559328117120
      }
    ]
  }
]
```

**Query for one particular product by id**

```
    /products/:id
```

Expected output should be similar to:

```json
{
  "id": "abc123",
  "transaction": [
    {
      "id": "abc123",
      "quantity": 123,
      "time": 1559328117100
    }
  ]
}
```

Notice querying all products returns all products in one array of object, single product returns only one product with that specific id.

## Part 2: GraphQL/Prisma

I should be able to query the same products with GraphQL.

```graphql
query products {
  products {
    id
    transactions {
      id
      quantity
      time
    }
  }
}
```

And then for single product:

```graphql
query product {
  product(id: "abc123") {
    id
    transactions {
      id
      quantity
      time
    }
  }
}
```

Expected output is same as Part 1: Rest API above.

## Part 3: GraphQL Subscriptions

Build a very minimal websocket and/or graphql subscription solution which sends updates to the client about single product.

So, whenever we add/remove/update a single transaction on any product, the playground/ws client should know about that specific post and transaction in some way.

Showcase/provide your own subscription resolver without us providing any specific format.

**Example workflow on playground:**

1. I am subscribing to products
2. on another tab I triggered **createProduct** mutation
3. on the subscribing tab, it shows something was created
4. I go back to other tab and trigger **createProduct** again
5. on the subscribing tab, it shows something was created

Link to sample video: https://www.youtube.com/watch?v=LVUEpv8Mvr0&