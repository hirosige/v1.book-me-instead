### Favorite

```js
type Favorite @model {
  id: ID! @isUnique

  createdAt: DateTime!
  updatedAt: DateTime!

  user: User! @relation(name: "UserFavorites")
  hotels: Hotel! @relation(name: "FavoriteHotels")
}

getMyFavoriteHotels()

```