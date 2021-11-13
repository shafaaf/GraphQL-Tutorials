## Graphql basics series using Apollo server:

From: https://www.youtube.com/watch?v=DyvsMKsEsyE&list=PLN3n1USn4xln0j_NN9k4j5hS1thsGibKi&ab_channel=BenAwad

Cheat sheet: https://wehavefaces.net/graphql-shorthand-notation-cheatsheet-17cd715861b6

- reolvers are impl of the functions and must respect the type specified in the typeDefs or else error when querying
- typeDefs are like function signatures for the queries, mutations and defining types like User, Error, ErrorResponse etc
 - can pass in headers, req, res object etc in context in resolvers
 - can resolver a type like User as well. In this case, can use parent to access that specific object properties
- when use resolver for a type can add in more fields that are computable fields like firstLetterOfUsername for User field
- resolvers can be async and call make db call etc

- subscriptions use websockets underneath


TODO: GraphQL Subscription video: https://www.youtube.com/watch?v=_r2ooFgBdoc&list=PLN3n1USn4xln0j_NN9k4j5hS1thsGibKi&index=4&ab_channel=BenAwad



Query at: http://localhost:4000/

```
 query BasicQuery {
  user {
    id
    username
  }
}
```

Mutiple queries:
query MultipleQueries {
  hello (name: "shafaaf")
  user {
    id
    username
  }
}

Example mutation:
mutation MyMutation {
  register (userInfo: {username: "Shafaaf", password: "myPassword", age: 12}) {
    errors {
      field
      message
    }
    user {
      id
      username
      firstLetterOfUsername
    }
  }
}

More complex:
query Complex {
  user {
    id
    username
    firstLetterOfUsername
  }
}
