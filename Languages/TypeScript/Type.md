The `type` keyword has 2 use cases

## Object Type

`type` can be used to describe the shape of an object.

```ts
type User = {
  username: string
  role: 'admin' | 'user' | 'modeator' | 'guest'
}

const user: User = {
  username: 'dnmct',
  role: 'guest'
}
```

## Type alias

A type alias is like a *binding* for types.
You can give a simpler name to a more complex type combination.
The benefit here is, to create reusable type, that only needs to be changed in one place.

```ts
type Role = 'admin' | 'user' | 'modeator' | 'guest'

type User = {
  username: string
  role: Role
}

const user: User = {
  username: 'dnmct',
  role: 'guest'
}
```



