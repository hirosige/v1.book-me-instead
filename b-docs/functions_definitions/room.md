### Room

```js
type Room @model {
  id: ID! @isUnique
  name: String!
  roomType: ROOM_TYPE @defaultValue(value: SUPERIOR)
  price: Float
  people: Int

  createdAt: DateTime!
  updatedAt: DateTime!

  photos: [File!]! @relation(name: "RoomPhotos")
  hotel: Hotel! @relation(name: "HotelRooms")
}
```