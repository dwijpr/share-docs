---
layout: post
title:  "ShareApp Initial version 0.0.1"
date:   2015-12-29 06:24:52 +0700
categories: version
---

## ShareApp



### App Info
- Programming Language: 
    - name: PHP
    - version: 5.5.9-1ubuntu4.14
- Framework: 
    - name: Laravel
    - version: 5.2.5
- Database: mysql  Ver 14.14 Distrib 5.6.27
- Server:
    - name: nginx + php5-fpm
    - version: 1.4.6 (Ubuntu)



### System Design


#### Entities:
- User
    - id ~ increments
    - name ~ string
    - email ~ string - unique
    - password ~ string|60
    - rememberToken
    - timestamps
    - softDeletes
- Password_reset
    - email ~ string - index
    - token ~ string - index
    - timestamp ~ created_at


#### Stories:
- User Register

    landing-page -> register -> user-home

- User Logout

    user-home -> logout -> landing-page

- User Login
    
    landing-page -> login-page -> user-home

- User Password Reset

    landing-page -> login-page -> password-reset

    user-get-email -> password-reset-token -> user-home

- Landing Page Access Prevention after Login

    landing-page -(redirect)-> user-home

- Prevent auth pages

    redirect -> login-page


#### Pages:
- /
- /register
- /home
- /login
- /password/reset
- /password/reset/{token}