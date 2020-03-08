##Restfull for yii 1 blog
A simple resftfull app with yii 1 

## Requirements

* PHP 5.4.0 (or later)*
* YiiFramework 1.1.14 (or later)
* PHPUnit 3.7 (or later) to run tests.

 _For older versions of PHP (< 5.4) checkout [v1.15](https://github.com/evan108108/RESTFullYii/tree/v1.15) or [cccssw's](https://github.com/cccssw) amazing 5.3 port: [https://github.com/cccssw/RESTFullYii](https://github.com/cccssw/RESTFullYii)_

## Installation
Create user and post tables

* ###tables
1. ####tbl_user
* id
* username
* password
* email

2. ###tbl_post

* id
* title
* content
* status
* tags
* auther_id (related to user id)

## How it works
RestfullYii extention adds a new set of RESTFul routes to your standard routes, but prepends '/api' .

So if you apply RestfullYii to the 'PostController' you will get the following new routes by default.

```
[GET] http://yoursite.com/api/post (returns all posts)
[GET] http://yoursite.com/api/post/1 (returns post with PK=1)
[POST] http://yoursite.com/api/post (create new post)
[PUT] http://yoursite.com/api/post/1 (update post with PK=1)
[DELETE] http://yoursite.com/api/post/1 (delete post with PK=1)
```

##notice:
you must be logged in for this requests.

in header request, set this parameters:
```
X-REST-USERNAME : admin@restuser
X-REST-PASSWORD : admin@Access  
```