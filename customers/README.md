# Customers

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
<div align="right">
  <b><a href="#customers">↥ Back To Top</a></b>
</div>
<br>

```
# Get customers updated after July 12, 2021
{
  customers(first: 10, query:"updated_at:>2021-07-12") {
    edges {
      node {
        id
        displayName
      }
    }
  }
}
```
<div align="right">
  <b><a href="#customers">↥ Back To Top</a></b>
</div>
<br>

```
# Get multiple customers using their IDs and GraphQL aliases
{
  customer1: customer(id:"gid://shopify/Customer/1310260264982") {
    displayName
  }
  customer2: customer(id:"gid://shopify/Customer/1310260789270") {
    displayName
  }
  customer3: customer(id: "gid://shopify/Customer/1310260854806") {
    displayName
  }
}
```

<div align="right">
  <b><a href="#customers">↥ Back To Top</a></b>
</div>
<br>

<div align="right">
  <b><a href="https://github.com/0l1v3r5/shopify-graphql-queries">↤ Back To Index</a></b>
</div>
