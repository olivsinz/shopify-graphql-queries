# GraphQL that return orders

```
# Get the first 10 orders
{
  orders(first: 10) {
    edges {
      node {
        id
      }
    }
  }
}

```
