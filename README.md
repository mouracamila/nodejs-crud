# NodeJS aplication with CRUD

## Introduction

This is aplication for a basic structure for project management.

### Technologies used and their definitions:

- **NodeJS**: As an asynchronous event-driven JavaScript runtime, Node.js is designed to build scalable network applications.
- **Express** : Framework for building web applications on top of NodeJS.
- **CRUD**: Acronum for **C**reate, **R**ead, **U**pdate and **D**elete. It is set of operation for servers to execute (POST, GET PUT and DELETE).
- **UUID** : Generator of unique identifiers for objects.
- **Query** parameters: Are a defined set of parameters attached to the end of a url. They are extensions of the URL that are used to help define specific content or actions based on the data being passed. Making filtering and paging possible.
- **JSON**: The json() method of the Body mixin takes a Response stream and reads it to completion. It returns a promise that resolves with the result of parsing the body text as JSON.
- **Nodemon**: Nodemon is a utility that will monitor for any changes in your source and automatically restart your server.

## Instalation

1. Clone this Repository:

   `$ git clone git@github.com:mouracamila/nodejs-crud.git`

2. Acess the `src` folder:

   `$ cd src`

3. Installing dependencies:

   `$ yarn`

4. Running project:

   `$ yarn dev`

After running the project, in your terminal, this message shold be displayed:

```
[nodemon] starting `node src`
 🚀 Back-end started!
```

### Create project

POST /projects

#### Parameters

| Name  | Type | Required | Description   |
| ----- | ---- | -------- | ------------- |
| title | any  | Yes      | Project title |
| owner | any  | Yes      | Project owner |

#### Responses

SUCCESS  
`Code: 200`

```
{
  "id": <tokenUUID>,
  "title": <any>,
  "owner": <any>
}

```

### Put project

PUT /projects

#### Parameters

| Name  | Type | Required | Description |
| ----- | ---- | -------- | ----------- |
| token | any  | Yes      | UUID Token  |

#### Responses

SUCCESS  
`Code: 200`

```
[]
```

ERROR  
`Code: 400`

```
{
  "error": "Project not found."
}
```

### Delete project

DEL /projects

#### Parameters

| Name  | Type | Required | Description |
| ----- | ---- | -------- | ----------- |
| token | any  | Yes      | UUID Token  |

#### Responses

SUCCESS

`Code: 200`

```

[]

```

ERROR

`Code: 400`

```

{
"error": "Project not found."
}

```

#### API Exemple:

```

{
"title": "React project",
"owner": "Ted"
}

```

#### Preview Exemple:

```

{
"id": "dabbe8e7-6d39-4c54-9ce1-310eb720915e",
"title": "React project",
"owner": "Ted"
}

```

### License

This project is under license from [MIT](https://en.wikipedia.org/wiki/MIT_License).

---

with ❤

```

```
