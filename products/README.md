# GraphQL that return Products

```
# Get the title and description of a product (Simple query)
{
  product(id: "gid://shopify/Product/1974208299030") {
    title
    description
  }
}

```

```
# Get the title and description of a product (more complex query)
{
  product(id: "gid://shopify/Product/1974208299030") {
    title
    description
    descriptionHtml
    inCollection(id: "gid://shopify/Collection/1974208299030")
    metafields(first: 5) {
      edges {
        node {
          key
          namespace
        }
      }
    }
    privateMetafields(first: 5) {
      edges {
        node {
          key
          namespace
        }
      }
    }
    images(first: 5, sortKey: POSITION) {
      edges {
        node {
          altText
          height
          width
          metafields(first: 5) {
            edges {
              node {
                key
                namespace
              }
            }
          }
          privateMetafields(first: 5) {
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
}
```

