## Typescript GraphQL tutorial

- Uses apollo-server-express
- Created from npx create-graphql-api <project_name>

Tutorial from: https://www.youtube.com/watch?v=WhzIjYQmWvs&ab_channel=BenAwad
Code: https://github.com/benawad/typescript-graphql-crud-example


GraphQL UI: http://localhost:4000/graphql

Example query:
```
query getAllMovies {
  movies {
     id
    title
  }
}
```

Example mutation:
```
mutation createMovie {
    createMovie (options: {title: "ShawShank", minutes: 72}) {
        id
        title
        minutes
    }
}
```
