## 0x0F. Python - Object-relational mapping

### Description
The goal of this project is to learn how to use an Object-relational mapper (ORM). We'll use the `MySQLdb` module in Python to connect to a MySQL database, and then the `SQLAlchemy` module for the ORM.

### Background Context
In this project, we'll bridge two amazing worlds: Databases and Python! Here's what we'll cover:

1. **MySQLdb Connection and SQL Queries**
   - We'll use the `MySQLdb` module to connect to a MySQL database and execute SQL queries directly.
   - Example (without ORM):
     ```python
     conn = MySQLdb.connect(host="localhost", port=3306, user="root", passwd="root", db="my_db", charset="utf8")
     cur = conn.cursor()
     cur.execute("SELECT * FROM states ORDER BY id ASC")
     query_rows = cur.fetchall()
     for row in query_rows:
         print(row)
     cur.close()
     conn.close()
     ```

2. **SQLAlchemy ORM**
   - We'll switch to using the `SQLAlchemy` ORM, which abstracts storage details.
   - No more direct SQL queries! We'll work with Python objects.
   - Example (with ORM):
     ```python
     engine = create_engine('mysql+mysqldb://{}:{}@localhost/{}'.format("root", "root", "my_db"), pool_pre_ping=True)
     Base.metadata.create_all(engine)
     session = Session(engine)
     for state in session.query(State).order_by(State.id).all():
         print("{}: {}".format(state.id, state.name))
     session.close()
     ```

### Files in this Directory
1. **`0-select_states.py`**: Retrieves all states from the database and prints them.
2. **`1-filter_states.py`**: Retrieves states starting with a specific letter (user-defined) and prints them.
3. **`2-my_filter_states.py`**: Retrieves states containing a specific letter (user-defined) and prints them.
4. **`3-my_safe_filter_states.py`**: Retrieves states containing a specific letter (user-defined, safe from SQL injection) and prints them.
5. **`4-cities_by_state.py`**: Retrieves cities associated with each state and prints them.
6. **`5-filter_cities.py`**: Retrieves cities containing a specific letter (user-defined) and prints them.
7. **`7-model_state_fetch_all.py`**: Retrieves all states using SQLAlchemy ORM and prints them.
8. **`8-model_state_fetch_first.py`**: Retrieves the first state using SQLAlchemy ORM and prints it.
9. **`9-model_state_filter_a.py`**: Retrieves states starting with the letter 'a' using SQLAlchemy ORM and prints them.
10. **`10-model_state_my_get.py`**: Retrieves a state by its ID using SQLAlchemy ORM and prints it.
11. **`11-model_state_insert.py`**: Inserts a new state using SQLAlchemy ORM.
12. **`12-model_state_update_id_2.py`**: Updates a state's name using SQLAlchemy ORM (state with ID 2).
13. **`13-model_state_delete_a.py`**: Deletes a state with the letter 'a' using SQLAlchemy ORM.
14. **`14-model_city_fetch_by_state.py`**: Retrieves cities along with their associated states using SQLAlchemy ORM.

### Resources
- [mysqlclient/MySQLdb documentation](https://mysqlclient.readthedocs.io/en/latest/)
- [SQLAlchemy tutorial](https://docs.sqlalchemy.org/en/20/tutorial/index.html)
- [Introduction to SQLAlchemy](https://www.tutorialspoint.com/sqlalchemy/sqlalchemy_introduction.htm)
- [Flask SQLAlchemy](https://flask-sqlalchemy.palletsprojects.com/)
- [10 common stumbling blocks for SQLAlchemy newbies](https://alextechrants.blogspot.com/2013/11/10-common-stumbling-blocks-for.html)
- [Python SQLAlchemy Cheatsheet](https://www.pythonsheets.com/notes/python-sqlalchemy.html)
- [SQLAlchemy ORM Tutorial for Python Developers](https://auth0.com/blog/sqlalchemy-orm-tutorial-for-python-developers/) (Note: This tutorial is with PostgreSQL, but the concept of SQLAlchemy is the same with MySQL)

Feel free to explore these files and dive into the world of Python ORM! 😊🐍🔍