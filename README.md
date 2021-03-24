# wrpt1-fullstack-review
E-commerce full stack project


## MVP

- users should be able to find products
- users should be able to purchase products - use stripe
- users should be able to register for an account, login, logout
- users should be albe to delete an account
- users should be able to have a cart

## ICEBOX

- login with social media, or 3rd party accounts
- clean error handling/ utility snack bars
- share product with another user
- admin UI
- SMS and Email features
- order history
- recommended products based on viewed or purchased products
- wishlist/like/favorite products
- product reviews and ratings


### Dependencies

- axios
- express
- massive
- express-session
- redux
- react-redux
- redux-promise-middleware
- redux-devtools
- react-router-dom
- react-toastify
- bcryptjs
- dotenv

## Database

### Tables
products
```SQL
    create table products(
    product_id serial primary key not null,
    category varchar(100),
    price decimal,
    description varchar(1000)
    );
    
```
product_images
```SQL
  create table product_images(
  product_images_id serial primary key not null,
  product id references products(product_id),
  url text
  );
```

users
```SQL
  create table users(
  user_id serial primary key not null,
  email varchar(500),
  password varchar(1000)
  );
```

## Server

### Controllers

- usersController
- productsController

### Endpoints

##### Products
- get all products => GET '/api/products'
- get specific products => POST '/api/products'
- 
##### Users
- register a user => POST '/api/register'
- login a user => POST '/api/login'
- logout a user => DELETE '/api/logout'
- delete a user => DELETE '/api/delete'

## Front-End
