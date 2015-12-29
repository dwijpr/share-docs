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

#### Pages:
- /
- /register
- /home
- /login
- /password/reset
- /password/reset/{token}

#### Stories:

<div class="panel panel-success">
    <div class="panel-heading">
        <h4 class="panel-title">
            User Register
        </h4>
    </div>
    <div class="panel-body">
        landing-page -> register -> user-home
    </div>
</div>

<div class="panel panel-primary">
    <div class="panel-heading">
        <h4 class="panel-title">
            User Logout
        </h4>
    </div>
    <div class="panel-body">
        user-home -> logout -> landing-page
    </div>
</div>

<div class="panel panel-default">
    <div class="panel-heading">
        <h4 class="panel-title">
            User Login
        </h4>
    </div>
    <div class="panel-body">
        landing-page -> login-page -> user-home
    </div>
</div>

<div class="panel panel-default">
    <div class="panel-heading">
        <h4 class="panel-title">
            User Password Reset
        </h4>
    </div>
    <div class="panel-body">
        landing-page -> login-page -> password-reset
        <br>
        user-get-email -> password-reset-token -> user-home
    </div>
</div>
    
<div class="panel panel-default">
    <div class="panel-heading">
        <h4 class="panel-title">
            Landing Page Access Prevention after Login
        </h4>
    </div>
    <div class="panel-body">
        landing-page -(redirect)-> user-home
    </div>
</div>

<div class="panel panel-default">
    <div class="panel-heading">
        <h4 class="panel-title">
            Prevent auth pages
        </h4>
    </div>
    <div class="panel-body">
        redirect -> login-page
    </div>
</div>

<div class="panel panel-default">
    <div class="panel-heading">
        <h4 class="panel-title">
            Pnotify
        </h4>
    </div>
    <div class="panel-body">
<pre>
    - error credentials user
        - type: error
        - title: Error Credentials
        - message: Unknown username or password

    - success logged in
        - type: success
        - title: Successfully Login
        - message: Hi {user}, Welcome!

    - logged out
        - type: info
        - title: Bye
        - message: Don't forget to come back

    - Unauthorized access
        - type: warning
        - title: Unauthorized Access
        - message: Please login first
</pre>
    </div>
</div>

<div class="panel panel-default">
    <div class="panel-heading">
        <h4 class="panel-title">
        </h4>
    </div>
    <div class="panel-body">
    </div>
</div>

