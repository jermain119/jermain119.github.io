---
layout: post
title:      "PARAMS[:PASSWORD]"
date:       2019-12-14 18:13:10 +0000
permalink:  params_password
---


A couple of days ago I had my Sinatra assessment for which I didn't do so good.
one of the reasons why I didn't do well on my assessment is because a lack of understanding of the concept of params
specifically how params are interlinked from the controller side to view side. 

here is a perfect example of the use of params

login.erb
```
<div class="container">
  <form action="/login" method="post">
    <h1>Welcome! Please Log In: </h1>
    <div class="form-group">
      <label for="user-email">Email </label>
      <input type="email" class="form-control" name="email" id="user-email">
    </div>
    <div class="form-group">
      <label for="user-password">Password </label>
      <input type="password" class="form-control" NAME="PASSWORD"  id="user-password">
    </d
    <button type="submit" class="btn btn-primary" id="btn-main">Log In</button>
  </form>
</div>

```

users_controller.rb
```
 post '/login' do
    user = User.find_by(:email => params[:email])
    if user && user.authenticate(PARAMS[:PASSWORD])
      session[:user_id] = user.id
      redirect '/books'
    else
      redirect to '/signup'
    end
  end
```

main parts that matter here within the two files are what is capittalize. without the params hash working in the users_controller.rb one would not be able to store the input data correctly you see in  `NAME="PASSWORD " ` tag in login.erb and set that equal to the hash key. 
If you recall a hash syntax looks like this `hash = {
  :cat => "meow"}`. so when a user inputs information in the input field from the form the data is stored within that hash key.
	
