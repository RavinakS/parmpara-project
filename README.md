## Basic Mysql implementation with knex

### Create Database

#### Fisrt table
 - 1 /registration a user (name, email, password) - post
 - 2 /profile-edit/:userId (name, email, password )-put
 - 3 /delete-user/:userId - delete

#### Second table
 - user_post (userId, ImgUrl, date, captionForImg) - post