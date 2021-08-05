
# Billing

## GraphQL queries that return Billing objects (AppCredit, AppPurchaseConfirmation, ...)

```
# Get the amount of the first 5 app credits that can be used towards future app purchases at Shopify
{
  appInstallation {
    credits(first: 5) {
      edges {
        node {
          amount {
            amount
          	currencyCode
          }
        }
      }
    }
  }
}
```

<div align="right">
  <b><a href="#billing">↥ Back To Top</a></b>
</div>
<br>

```
# Get the date and time when the app credits were created
{
  appInstallation {
    credits(first: 5) {
      edges {
        node {
          createdAt
        }
      }
    }
  }
}
```
<div align="right">
  <b><a href="#billing">↥ Back To Top</a></b>
</div>
<br>

```
# Get information about whether the app credits are test transactions
{
  appInstallation {
    credits(first: 5) {
      edges {
        node {
          test
        }
      }
    }
  }
}
```

<div align="right">
  <b><a href="#billing">↥ Back To Top</a></b>
</div>
<br>

<div align="right">
  <b><a href="https://github.com/0l1v3r5/shopify-graphql-queries">↤ Back To Index</a></b>
</div>
