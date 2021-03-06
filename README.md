# notex-back
Note taking app for the JKUAT GDG talk using Node.js, Express, Sequelize and Postgres.

## How to run the app
- Clone the repo `$git clone https://github.com/ronaldndirangu/notex-back.git`
- Cd into the `$cd notex-back` directory.
- Install the dependancies using `$yarn install`
- Add the env variable using a `.env` file in the root dir. The required variables are as in the `env.evample`
- Run `$yarn db:rollmigrate` to rollback and migrate the database.
- Start the server by running `$yarn start`

## Endpoints
Method | Endpoint | Task | Requires Auth
------- | ------------ | ------------- | -----------
POST | `/api/v1/auth/signin` | User can login to the application | No
POST | `/api/v1/auth/signup` | User can signup for the application | No
POST | `/api/v1/notes` | User can create a note | Yes
GET | `/api/v1/notes` | User can view all his/her notes | Yes
PATCH | `/api/v1/notes/:id` | User can edit a specific note | Yes
GET | `/api/v1/notes/:id` | User view a specific note | Yes
DELETE | `/api/v1/notes/:id` | User can delete a specific note | Yes

## Notes
- To use token for authentication add it to the `headers` using the `Authorization` key.
