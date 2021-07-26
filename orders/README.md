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
