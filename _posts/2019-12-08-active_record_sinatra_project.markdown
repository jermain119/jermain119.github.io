---
layout: post
title:      "ACTIVE RECORD SINATRA PROJECT"
date:       2019-12-08 12:52:34 -0500
permalink:  active_record_sinatra_project
---

 one of the most enjoyable and interesting section for this project for me was the database portion and how macro programming creates this seamless feel of code that enable the use of our database to link the database to our app model file. what is macro-programming you ask? in a nutshell it is code that writes itself. Two common macros are the `belongs_to`and`has_many` macros an example of such macros in an object are `, class
  belongs_to :user
end` and ` class 
has_many :books
end ` I want to take a minute to explain the level of helpfulness that the macros do by breaking what this code would look like without macros `def self.has_many(books)
  puts "#{self} has many #{books}"

  def users(belongs_to)
    puts "how to kill a mockingbird"
  end `  going from this to `has_many` macro cuts down on the time of hard coding all this function and lets you worry about other aspects of your program. 
