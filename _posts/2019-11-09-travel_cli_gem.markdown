---
layout: post
title:      "travel cli gem "
date:       2019-11-09 20:37:40 +0000
permalink:  travel_cli_gem
---


A little about my background in the tech world started the day I decided to enroll in college to obtain a bachelor's in computer science. I made it somewhere in between that with an associate's degree in computer science well at least that is what my classification says. but outside of that, I have always been a person who has been fascinated with the science world so many possibilities to branch off from which has to lead me to where I am currently a full-stack developer in training. 

on to my CLI gem project, I have created an app that prints out to the user the top ten landmarks of Barcelona from a website I scraped called www.tripadvisor.com. why make a travel CLI on Barcelona landmarks you may ask? well, I like Spanish and I love to travel so it seemed like the obvious choice.  After printing out the landmarks you make a selection from there, picking a number [0..10]  After this the program puts out your choice after that the program repeats itself self or you can exit it by typing no or exit. my project is very simple and basic nothing complex or amazing. What I will be sharing with you is a snippet from my project and talk some terminology about the snippet. The code that is displayed below is one of three files that makes up the bulk of the code that is needed to create a functional app.

**example **
```

class Cli
  
  def run 
      self.greeting
      Scraper.scrape_landmarks
      loop do 
      user_input = main_menu
      if user_input == "exit" || user_input.include?("n")
      return 
          
        else 
        self.list_landmarks
        self.choose_landmarks
        
        end
      end
  end 
    
    
end
```
 
 Starting with the class CLI portion of code. 
 
 ``` class  Cli 
 
     def example
         
           [some code]
         
         end
         
  end ``` 
 
 Think of this as the (bowl that holds all the other pieces together. (note that a class object starts with a CAPITAL letter after the word class). these pieces inside the bowl are called methods they look like this inside a program ``` def example  [some code]  end```. The code 
 ```def begin
        [some code]
      end```  The alignment of ```def    end ```are very important although there want to be a syntax era when you execute the program in ruby, it is still important for you and people reading your code to know what is what.   Moving down the code we see ```self.greeting  Scraper.scrape_landmarks  self.list_landmarks  self.choose_landmarks ``` the dot is linking a  method to an object this object is called a class object.  The last piece of code is what is called a iterator that looks like this ```loop do  [some code] end```    think of the loop do iterator as if you were on an endless roller coaster that never stops. The endless roller coaster would be the loop do and if you wanted to get out of this loop you would have to put in a ```return ``` keyword or ```break``` keyword as you see in the above snippet. The ```if [some condition]  else[somecode] end ```  think of this as adding another maneuver to the roller coaster if some condition is met it will do this That concludes the end of this blog.
