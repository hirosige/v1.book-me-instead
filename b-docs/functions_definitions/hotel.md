### Hotel

```js
type Hotel @model {
  id: ID! @isUnique
  name: String! @isUnique
  address: String!
  latitude: Float
  longitude: Float
  appliances: String!
  tel: String!
  fax: String
  email: String!
  isPublished: Boolean! @defaultValue(value: "false")

  createdAt: DateTime!
  updatedAt: DateTime!

  country: Country! @relation(name: "CountryHotels")
  area: Area! @relation(name: "AreaHotels")
  rooms: [Room!]! @relation(name: "HotelRooms")
  photos: [File!]! @relation(name: "HotelPhotos")
  favorites: [Favorite!]! @relation(name: "FavoriteHotels")
  advantages: [Advantage!]! @relation(name: "HotelsAdvantages")

  bookings: [Booking!]! @relation(name: "HotelBookings")
  reviews: [Review!]! @relation(name: "HotelReviews")
}

getNearbyHotels()
getHotelsInCountry()
getHotelsInArea()
getFavoriteCount()

```