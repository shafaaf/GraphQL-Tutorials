## Graphql basics

- Uses express-graphql

#### Authors-Books relationship

From: https://www.youtube.com/watch?v=ZQL7tL2S0oQ&ab_channel=WebDevSimplified

Code: https://github.com/WebDevSimplified/Learn-GraphQL

Graphql UI at: http://localhost:5000/graphql

Example graphql queries at Graphql UI: 

query {
    authors {
        id
        name
        books {
            id
            name
        }
    }
}

query {
    author(id: 1) {
        id
        name
        books {
            id
        }
    }
}

mutation {
    addBook (name: "RANODM book", authorId: 1)
}
