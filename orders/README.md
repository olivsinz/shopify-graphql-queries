# Orders

# GraphQL queries that return orders

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

<div align="right">
<b><a href="#orders">↥ Back To Top</a></b>
</div>
<br>

```
# Get the first 10 orders with authorized payments
{
  orders(first:10, query:"financial_status:AUTHORIZED") {
    edges {
      node {
        id
        displayFinancialStatus
      }
    }
  }
}
```

<div align="right">
<b><a href="#orders">↥ Back To Top</a></b>
</div>
<br>

```
# Get a list of orders using their IDs and GraphQL aliases
{
  order1: order(id:"gid://shopify/Order/1248358563862") {
  	name
  }
  order2: order(id:"gid://shopify/Order/1248358694934") {
    name
  }
}
```

<div align="right">
  <b><a href="#orders">↥ Back To Top</a></b>
</div>
<br>

```
# Get an order by its ID (more complex query)
{
  order(id: "gid://shopify/Order/1248358563862") {
    name
    canMarkAsPaid
    canNotifyCustomer
    clientIp
    closedAt
    currencyCode
    customerLocale
    discountCode
    paymentGatewayNames
    displayAddress {
      id
    }
    customer {
      displayName
      email
    }
    customerJourneySummary {
      daysToConversion
      firstVisit {
        marketingEvent {
          utmMedium
          utmCampaign
          app {
            appStoreAppUrl
            appStoreDeveloperUrl
            developerName
          }
        }
      }
    }
    customAttributes {
      key
      value
    }
    billingAddress {
      firstName
      lastName
      address1
      address2
      city
      company
      country
      countryCodeV2
      formattedArea
      latitude
      longitude
      phone
      name
      province
      zip
    }
    events(first: 10, sortKey: CREATED_AT){
      edges{
        node {
          appTitle
          attributeToUser
          criticalAlert
          message
        }
      }
    }
  }
}

```

<div align="right">
  <b><a href="#orders">↥ Back To Top</a></b>
</div>
<br>

<div align="right">
  <b><a href="https://github.com/0l1v3r5/shopify-graphql-queries">↤ Back To Index</a></b>
</div>
