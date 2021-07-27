# Shopify Payments

## GraphQL queries

```
# Get the IDs of the first 10 bank accounts
{
  shopifyPaymentsAccount {
    bankAccounts(first:10) {
      edges {
        node {
          id
          accountNumber
          accountNumberLastDigits
          bankName
          createdAt
          currency
          routingNumber
          status
        }
      }
    }
  }
}
```
<div align="right">
  <b><a href="#shopify-payments">↥ Back To Top</a></b>
</div>
<br>

```
# Get the IDs of the first 10 payouts
{
  shopifyPaymentsAccount {
    payouts(first:10) {
      edges {
        node {
          id
        }
      }
    }
  }
}
```

<div align="right">
  <b><a href="#shopify-payments">↥ Back To Top</a></b>
</div>
<br>

<div align="right">
  <b><a href="https://github.com/0l1v3r5/shopify-graphql-queries">↤ Back To Index</a></b>
</div>
