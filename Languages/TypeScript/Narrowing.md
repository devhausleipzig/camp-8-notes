We don't always exactly know what type we are working with, it could be that a function we wrote can take an arguemnt that has a union type.

## in operator

The in operator allows us to quickly determine the type of an argument, if the arguement is of a union type.

```ts
type User = {
  username: string
  password: string
}

const user: User = {
  username: "dnmct",
  password: "slkdjakls"
}

type Admin = {
  username: string
  password: string
  permissions: string[]
}

const admin: Admin = {
  username: "admin1",
  password: "alksdja",
  permissions: ['edit', 'read']
}

function getPersonType(person: Admin | User): 'user' | 'admin' {
  // person -> Admin | User
  if('permissions' in person) {
	// person -> Admin
	person.permissions // valid
    return 'admin'
  } else {
	// person -> User
	person.permissions // invalid
    return 'user'
  }
}

console.log(getPersonType(admin))
```

## type predicates

```ts
type User = {
  username: string;
  password: string;
};

const user: User = {
  username: "dnmct",
  password: "slkdjakls",
};

type Admin = {
  username: string;
  password: string;
  permissions: string[];
  zip: string;
};

const admin: Admin = {
  username: "admin1",
  password: "alksdja",
  permissions: ["edit", "read"],
  zip: "04318",
};

type Moderator = {
  username: string;
  password: string;
  permissions: string[];
};

const moderator: Moderator = {
  username: "admin1",
  password: "alksdja",
  permissions: ["edit", "read"],
};

function isModerator(person: User | Moderator): person is Moderator {
  return (person as Moderator).permissions !== undefined;
}

function isAdmin(person: Admin | User | Moderator): person is Admin {
  return (
    (person as Admin).permissions !== undefined &&
    (person as Admin).zip !== undefined
  );
}

function getPersonType(
  person: Admin | User | Moderator
): "user" | "admin" | "moderator" {
  // person -> Admin | User | Moderator
  if (isAdmin(person)) {
    // person -> Admin
    return "admin";
  }
  // person -> User | Moderator
  if (isModerator(person)) {
    // person -> Moderator
    return "moderator";
  }
  // person -> User
  return "user";
}

console.log(getPersonType(moderator)); // -> moderator

```