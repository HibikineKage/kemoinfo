# kemoinfo
Fursuit database system

## スタック

* MySQL
* React
* Material-UI
* Go
* GraphQL
* (Redux)

## GraphQL API

```graphql
type User {
  userId: ID!
  name: String!
  felicaIDm: String
  email: String
  links: [Link!]
}
type Fursuit {
  fursuitId: ID!
  name: String!
  birthday: Date
}
type Link {
  user: User!
  type: String!
  value: String!
}
```

## DB

* user
  - user_id(UNIQUE)
  - name
  - id_name(UNIQUE)
  - felica_idm(UNIQUE)
  - email(UNIQUE)
  - email_verified
* fursuit
  - fursuit_id(UNIQUE)
  - user
  - name
  - color
  - birthday(Date,NULL)
* tagmap
  - fursuit_id
  - tag_id
* tag
  - tag_id(UNIQUE)
  - tag_name(UNIQUE)
