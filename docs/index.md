# Jelajah Nusantara API Documentation

In this documentation you will find all the information you need to use the [Jelajah Nusantara API](<[#](https://api-beta-testing.uc.r.appspot.com/)>).

Jika ingin melihat versi web dari aplikasi ini, silahkan kunjungi [Jelajah Nusantara](<[#](https://capstone-project-api-ch2-ps352.et.r.appspot.com/)>).

```bash
 https://capstone-project-api-ch2-ps352.et.r.appspot.com/web
```


## Base URL


Endpoint Base URL: `Beta Testing`

```bash
https://api-beta-testing.uc.r.appspot.com/
````

Endpoint Base URL: `Production`

```bash
https://capstone-project-api-ch2-ps352.et.r.appspot.com/
```

## Auth

This page [auth](https://buryne.github.io/capstone-api-docs/auth/login/)

## Endpoint list post

| Method | Endpoint       | Description                                                                      |
| ------ | -------------- | -------------------------------------------------------------------------------- |
| GET    | /api/posts     | Get all posts.                                                                   |
| POST   | /api/posts     | Create a new post.                                                               |
| PUT    | /api/posts/:id | Update an existing post. Only the **`user`** who created the post can update it. |
| GET    | /api/posts/:id | Retrieve information about a specific post.                                      |
| DELETE | /api/posts/:id | Delete an existing post. Only the user who created the post can delete it.       |

## Endpoint list user

| Method | Endpoint       | Description                                 |
| ------ | -------------- | ------------------------------------------- |
| GET    | /api/users     | Get all users.                              |
| GET    | /api/users/:id | Retrieve information about a specific post. |
