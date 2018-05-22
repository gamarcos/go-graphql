### Golang + graphQL

`
fragment PostFragment on Post {
  id
  title
  body: body
}

fragment WithComments on Post {
  comments {
    id
    email
    name
  }
}

{
  post(id: 5) {
    ...PostFragment
    ...WithComments
  }
}
`