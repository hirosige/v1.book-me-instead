### Profile

```js
type Profile @model {
  id: ID! @isUnique
  firstName: String
  lastName: String
  address: String
  tel: String
  subscriptionEmail: String

  createdAt: DateTime!
  updatedAt: DateTime!

  user: User! @relation(name: "UserProfile")
}
```