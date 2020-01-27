---
layout: post
title:      "Active Record Associations prep"
date:       2020-01-27 22:31:55 +0000
permalink:  active_record_associations_prep
---


I had the hardest time setting up my association because i didn't understand the proper relationships between has_many through.  there is a tool that helps you set up the relationships between your models. I would advise anybody who cants grasp the understanding of the related association to use this tool which is called " Draw" the tool lets you put models together by shapes and lines corresponding to the shapes.

my app is a recipe app that lets you create, edit and delete a recipe. The models I used were recipes,  user and category.  here is a snippet of my models 
```
class Recipe < ApplicationRecord
    belongs_to :user
    belongs_to :category 
        end
    ```
        
    recipe belongs_to category and user
    
    ```
class Category < ApplicationRecord
  has_many :recipes
  has_many :users, through: :recipes
end
```

the category has_many recipes and many users through recipes

```
class User < ApplicationRecord

  has_many :recipes
  has_many :categories, through: :recipes
end

```

The last one is user models something to point out is that if you look at the Category model and User model the second has_many in both of these models are inverses of each other. these are important because a user has to go through Category to get to recipes.

this is it, for now, thanks for reading bye!
