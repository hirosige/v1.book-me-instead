### Review

```js
type Review @model {
  id: ID! @isUnique
  rating: Float!
  description: String!

  createdAt: DateTime!
  updatedAt: DateTime!

  hotel: Hotel! @relation(name: "HotelReviews")
  user: User! @relation(name: "UserReviews")
}
```