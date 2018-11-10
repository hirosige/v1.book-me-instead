### Tag

```js
type Tag @model {
  id: ID! @isUnique
  name: String! @isUnique
  color: String! @defaultValue(value: "#007bff")

  createdAt: DateTime!
  updatedAt: DateTime!

  posts: [Post!]! @relation(name: "PostTags")
}
```