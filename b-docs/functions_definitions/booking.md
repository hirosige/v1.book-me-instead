### Booking

```js
// TODO
type Booking @model {
  id: ID! @isUnique
  isPaid: Boolean! @defaultValue(value: "false")
  isConfirmed: Boolean! @defaultValue(value: "false")
  checkIn: DateTime!
  checkOut: DateTime!

  createdAt: DateTime!
  updatedAt: DateTime!

  hotel: Hotel! @relation(name: "HotelBookings")
  user: User! @relation(name: "UserBookings")
}

getPaidBookings()
getUnPaidBookings()
getConfirmedBookings()
getUnConfirmedBookings()
makeAnPayment()

```