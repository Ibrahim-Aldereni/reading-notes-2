# **GraphQL @connection:**

- The @connection directive enables you to specify relationships between @model types. this supports:(1)

  - one-to-one
  - one-to-many
  - many-to-one relationships.

- Definition:

  ```java
  directive @connection(keyName: String, fields: [String!]) on FIELD_DEFINITION
  ```

- One to one example: (project has one team)

  ```java
    type Project @model {
    id: ID!
    name: String
    teamID: ID!
    team: Team @connection(fields: ["teamID"])
  }

  type Team @model {
    id: ID!
    name: String!
  }
  ```

- One to many:(Post that can have many comments)

  ```java
  type Post @model {
  id: ID!
  title: String!
  comments: [Comment] @connection(keyName: "byPost", fields: ["id"])
  }

  type Comment @model
    @key(name: "byPost", fields: ["postID", "content"]) {
    id: ID!
    postID: ID!
    content: String!
  }
  ```

- Many to many:

  ```java
  type Post @model {
  id: ID!
  title: String!
  editors: [PostEditor] @connection(keyName: "byPost", fields: ["id"])
  }

  type PostEditor
    @model(queries: null)
    @key(name: "byPost", fields: ["postID", "editorID"])
    @key(name: "byEditor", fields: ["editorID", "postID"]) {
    id: ID!
    postID: ID!
    editorID: ID!
    post: Post! @connection(fields: ["postID"])
    editor: User! @connection(fields: ["editorID"])
  }

  type User @model {
    id: ID!
    username: String!
    posts: [PostEditor] @connection(keyName: "byEditor", fields: ["id"])
  }
  ```

## Sources:

- (1) [GraphQL @connection section](https://docs.amplify.aws/cli/graphql-transformer/connection/)

[Back to home page](../README.md)
