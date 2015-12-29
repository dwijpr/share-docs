---
layout: post
title:  "Sprint I - Login User System"
date:   2015-12-29 00:00:00 +0700
categories: version
---

## Stories:

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

<div class="panel panel-success">
    <div class="panel-heading">
        <h4 class="panel-title">
            User Logout
        </h4>
    </div>
    <div class="panel-body">
        user-home -> logout -> landing-page
    </div>
</div>

<div class="panel panel-success">
    <div class="panel-heading">
        <h4 class="panel-title">
            User Login
        </h4>
    </div>
    <div class="panel-body">
        landing-page -> login-page -> user-home
    </div>
</div>

<div class="panel panel-success">
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
    
<div class="panel panel-success">
    <div class="panel-heading">
        <h4 class="panel-title">
            Landing Page Access Prevention after Login
        </h4>
    </div>
    <div class="panel-body">
        landing-page -(redirect)-> user-home
    </div>
</div>

<div class="panel panel-success">
    <div class="panel-heading">
        <h4 class="panel-title">
            Prevent auth pages
        </h4>
    </div>
    <div class="panel-body">
        redirect -> login-page
    </div>
</div>

<div class="panel panel-success">
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
