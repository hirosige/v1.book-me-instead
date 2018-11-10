### Country

```js
type Country @model {
  id: ID! @isUnique
  name: String! @isUnique
  code: String! @isUnique
  slug: String! @isUnique

  createdAt: DateTime!
  updatedAt: DateTime!

  areas: [Area!]! @relation(name: "CountryAreas")
  hotels: [Hotel!]! @relation(name: "CountryHotels")
}

getCount()

```