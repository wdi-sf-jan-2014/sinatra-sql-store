# Managing Products with Sinatra and SQL

Your company has a working interface written with Sinatra and SQL to manage a list of products in your store.  The manager can add products, edit them, remove them, and view them.

We need a new feature: categories.  

1. Products should be in many categories, and categories should have many products.  
1. The manager should be able to create and delete categories.
1. The manager should be able to see all categories
1. The manager should be able to go to a category's page and view all the products in that category.
1. The manager should be able to go to a product's page and view all the categories that product is in.
1. From a product's edit form page, he should also be able to add and remove category memberships for that product.

Build this new functionality starting from the sinatra app for products in app.rb and views/.  Use the current functionality as a guide where possible.

You'll need to create the database from psql with `CREATE DATABASE <dbname>`.  Make sure the database in your postgres server has the same name as dbname in the app.rb.

You can run the table creation methods by requiring 'app.rb' and running the methods from pry.

If you create the database, run `create_products_table`, then run `seed_products_table`, you'll get some seed data for the products.  Writing some data of your own for the categories might be helpful.

BONUS: Make it pretty (I'm partial to lilacs).

BONUS: Refactor the database connection code into a method.  Use blocks and yield to make sure that the connection is always closed after the SQL commands are issued. Hint: (`with_db do | c | ... end`).

BONUS: On the categories page, the manager should be able to see the number of products in each category.

