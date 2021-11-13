## Graphql with Node, MongoDB

From: https://www.youtube.com/watch?v=YFkJGEefgU8&t=335s&ab_channel=BenAwad

# Write your query or mutation here
```
query {
  cats {
    id
    name
  }
}
```

```
mutation {
    createCat (name: "Garfield") {
        id
        name
    }
}
```
