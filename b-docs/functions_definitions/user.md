### User

```js
type User @model {
  id: ID! @isUnique
  email: String
  auth0UserId: String @isUnique
  role: ROLE! @defaultValue(value: USER)

  createdAt: DateTime!
  updatedAt: DateTime!

  avatar: File @relation(name: "Avatar")
  posts: [Post!]! @relation(name: "UserPosts")
  profile: Profile @relation(name: "UserProfile")
  favorites: [Favorite!]! @relation(name: "UserFavorites")

  bookings: [Booking!]! @relation(name: "UserBookings")
  reviews: [Review!]! @relation(name: "UserReviews")
}

setCloudinaryAvatar()

```