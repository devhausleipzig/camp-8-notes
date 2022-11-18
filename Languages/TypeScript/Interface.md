Interfaces and Types are alsmost feature-equal. There are slight differences in syntax

```ts
type User = {
	username: string
	role: string
}

interface User {
	username: string
	role: string
}
```

The main feature of an interface is the ability to extend other interfaces or types.

```ts

type WithPosts = {
	posts: string[]
}

interface User {
  username: string
  password: string
}

interface Admin extends User, WithPosts {
  permissions: string[]
}

const admin: Admin = {
  permissions: ['canEdit'],
  username: "user",
  password: "supersecret",
  posts: []
}
```