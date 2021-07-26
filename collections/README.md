
# Collections

## GraphQL queries that return collections

```
# Get the first 10 collections
{
  collections(first: 10) {
    edges {
      node {
        id
      }
    }
  }
}
```

<div align="right">
  <b><a href="#collections">↥ Back To Top</a></b>
</div>
<br>

```
# Get a collection by its ID
{
  collection(id: "gid://shopify/Collection/70598819862") {
    title
  }
}
```

<div align="right">
  <b><a href="#collections">↥ Back To Top</a></b>
</div>
<br>

```
# Get a collection using the QueryRoot.node field and a GraphQL fragment (Simple query)
{
  node(id:"gid://shopify/Collection/70598819862") {
    id
    ...on Collection {
      title
    }
  }
}
```

<div align="right">
  <b><a href="#collections">↥ Back To Top</a></b>
</div>
<br>

```
# Get a collection using the QueryRoot.node field and a GraphQL fragment (More complex query)
{
  node(id: "gid://shopify/Collection/70598819862") {
    id
    ... on Collection {
      handle
      title
      productsCount
      products(first: 10, sortKey: BEST_SELLING) {
        edges {
          node {
            title
          }
        }
      }
      metafields(first: 10) {
        edges {
          node {
            key
            namespace
          }
        }
      }
      privateMetafields(first: 10) {
        edges {
          node {
            key
            namespace
          }
        }
      }
      image {
        altText
        height
        width
        metafields(first: 10) {
          edges {
            node {
              key
              namespace
            }
          }
        }
        privateMetafields(first: 10) {
          edges {
            node {
              key
              namespace
            }
          }
        }
      }
    }
  }
}

```

<div align="right">
  <b><a href="#collections">↥ Back To Top</a></b>
</div>
<br>

<div align="right">
  <b><a href="https://github.com/0l1v3r5/shopify-graphql-queries">↤ Back To Index</a></b>
</div>
