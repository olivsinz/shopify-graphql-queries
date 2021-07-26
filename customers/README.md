# GraphQL queries that return customers

```
# Get the first 10 customers
{
  customers(first: 10) {
    edges {
      node {
        id
        displayName
      }
    }
  }
}

```
