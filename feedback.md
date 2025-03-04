Gabriel,
Your Hackathon project is great! I really like the idea and the final result.
Even though you didn’t achieve the exact result you were hoping for, you didn’t give up, and that’s what truly matters.
You used all the topics and tools we learned in class.
The code is readable, clean, and well-structured.
Also, just so you know, in the wishlist file, before creating the table wishlist you execute a query to delete the table if exist:
    cursor.execute(f'''DROP TABLE IF EXISTS {wishlist_name}''')
          cursor.execute(f'''CREATE TABLE {wishlist_name} (
                                  destination_id SERIAL PRIMARY KEY,
                                  country_name VARCHAR(100),
                                  city_name VARCHAR(100),
                                  temp INT,
                                  humidity INT)''')
          connection.commit()

You can simplify it like this:
    cursor.execute(f'''CREATE TABLE IF NOT EXISTS {wishlist_name} (
                            destination_id SERIAL PRIMARY KEY,
                            country_name VARCHAR(100),
                            city_name VARCHAR(100),
                            temp INT,
                            humidity INT)''')
    connection.commit()

You did an excellent job!
