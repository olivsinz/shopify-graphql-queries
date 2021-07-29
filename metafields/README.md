# Metafields

# GraphQL that return metafields

```
# Query a specific metafield using the `node` field and a GraphQL fragment
{
  node(id:"gid://shopify/Metafield/4148556103736") {
    id
    ... on Metafield {
      namespace
      key
      value
      type
      ownerType
      createdAt
    }
  }
}
```
<div align="right">
  <b><a href="#metafields">↥ Back To Top</a></b>
</div>
<br>

```
# Query a specific metafield by its namespace and key
{
  product(id:"gid://shopify/Product/1974208397334") {
    metafield(namespace: "instructions", key: "wash") {
      id
      value
      description
      createdAt
      updatedAt
      type
      ownerType
      description
      legacyResourceId
    }
  }
}
```
<div align="right">
  <b><a href="#metafields">↥ Back To Top</a></b>
</div>
<br>

```
# Query a product's first 20 metafields
{
  product(id:"gid://shopify/Product/1974208397334") {
    metafields(first: 20) {
      pageInfo {
        hasNextPage
        hasPreviousPage
      }
      edges {
        node {
          id
          namespace
          
          value
          description
          legacyResourceId
        }
      }
    }
  }
}
```

<div align="right">
  <b><a href="#metafields">↥ Back To Top</a></b>
</div>
<br>

```
# Query a resources's first 10 private metafields
{
  product(id:"gid://shopify/Product/10079785100") {
    privateMetafields(first:10) {
      edges {
        node {
          id
          namespace
          key
          value
          valueType
        }
      }
    }
  }
}
```

<div align="right">
  <b><a href="#metafields">↥ Back To Top</a></b>
</div>
<br>

```
# Query a specific private metafield using the `node` field and a GraphQL fragment
{
  node(id:"gid://shopify/PrivateMetafield/6291512") {
    ...on PrivateMetafield {
      id
      namespace
      key
      value
      valueType
    }
  }
}
```
<div align="right">
  <b><a href="#metafields">↥ Back To Top</a></b>
</div>
<br>

```
# Query a resource's private metafields using the `privateMetafields` connection on the QueryRoot
{
  privateMetafields(first:10, owner:"gid://shopify/Product/10079785100") {
    edges {
      node {
        id
        namespace
        key
        value
        valueType
      }
    }
  }
}
```

<div align="right">
  <b><a href="#metafields">↥ Back To Top</a></b>
</div>
<br>

<div align="right">
  <b><a href="https://github.com/0l1v3r5/shopify-graphql-queries">↤ Back To Index</a></b>
</div>
