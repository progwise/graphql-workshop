# Workshop

## 1. Hello World

Presentation:

```graphql
type Query {
  hello: String!
}
```

```graphql
type Query {
  hello(name: String): String!
}
```

Task:

> Create a query field `add` which takes the int arguments `a` and `b` and returns the argument sum.

## 2. New Type

Presentation:

```graphql
type Query {
  books: [Book!]!
  book(id: ID!): Book
}

type Book {
  id: ID!
  name: String!
  publishingYear: Int!
}
```

Task:

> Create a type `Author` with the fields `id`, `name` and `birthYear`.
> Create the query fields `authors: [Author!]!` and `author(id: ID!): Author`.

## 3. Connect Types

Presentation:

```graphql
  type Book {
    ...
+   author: Author!
  }
```

Task:

> Create the field `books` in type `Author`.

## 4. Mutation

Presentation:

```graphql
type Mutation {
  createAuthor(name: String!, birthYear: Int!): Author!
}
```

Task:

> Create the mutations `updateAuthor` and `deleteAuthor`.
> Optional: Add create/update/delete mutations for books.

## 5. Input fields

Presentation:

```graphql
input AuthorInput {
  name: String!
  birthYear: Int!
}
```
