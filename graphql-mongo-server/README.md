## Graphql with Node, MongoDB

- Uses apollo-server-express

From: https://www.youtube.com/watch?v=YFkJGEefgU8&t=335s&ab_channel=BenAwad

For setup, put in .env file in root folder
```
MONGODB_USERNAME = 'sha***'
MONGODB_PASSSWORD = 'yn***p5'
CLUSTER_URL = 'cluster0***'
```
Get these from memos doc, search "mongo"


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
