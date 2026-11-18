# Backend Tutorial

Completed backend from [Shivani’s freeCodeCamp tutorial](https://www.youtube.com/watch?v=KOutPbKc9UM).

## Run

```sh
npm install
cp .env.example .env
```

Set `MONGODB_URI` in `.env` to your MongoDB Atlas connection string, then run:

```sh
npm run dev
```

## Test with Postman

Use `http://localhost:4000` and select **Body → raw → JSON** for POST and PATCH requests.

| Method | Endpoint | JSON body |
| --- | --- | --- |
| POST | `/api/v1/users/register` | `{"username":"rahul","email":"rahul@example.com","password":"password123"}` |
| POST | `/api/v1/users/login` | `{"email":"rahul@example.com","password":"password123"}` |
| POST | `/api/v1/users/logout` | `{"email":"rahul@example.com"}` |
| POST | `/api/v1/posts/create` | `{"name":"Rahul","description":"My first post","age":20}` |
| GET | `/api/v1/posts/getPosts` | — |
| PATCH | `/api/v1/posts/update/:id` | `{"description":"Updated post"}` |
| DELETE | `/api/v1/posts/delete/:id` | — |

Replace `:id` with the `_id` returned when creating a post.

The login and logout endpoints follow the tutorial; they do not issue tokens or create sessions.
