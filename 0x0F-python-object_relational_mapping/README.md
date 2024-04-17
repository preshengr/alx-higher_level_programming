# 0x0F Python - Object Relational Mapping

This directory contains Python scripts that demonstrate the concept of Object Relational Mapping (ORM) using SQLAlchemy and MySQLdb.

## Files

- **0-select_states.py**: Script that lists all states from the database `hbtn_0e_0_usa`.
- **1-filter_states.py**: Script that lists all states with a name starting with 'N' from the database `hbtn_0e_0_usa`.
- **2-my_filter_states.py**: Script that takes in an argument and displays all values in the `states` table where `name` matches the argument.
- **3-my_safe_filter_states.py**: Script that is safe from MySQL injections.
- **4-cities_by_state.py**: Script that lists all cities from the database `hbtn_0e_4_usa`.
- **5-filter_cities.py**: Script that takes in the name of a state as an argument and lists all cities of that state.
- **7-model_state_fetch_all.py**: Script that lists all `State` objects from the database `hbtn_0e_6_usa`.
- **8-model_state_fetch_first.py**: Script that prints the first `State` object from the database `hbtn_0e_6_usa`.
- **9-model_state_filter_a.py**: Script that lists all `State` objects that contain the letter 'a' from the database `hbtn_0e_6_usa`.
- **10-model_state_my_get.py**: Script that prints the `State` object with the name passed as argument from the database `hbtn_0e_6_usa`.
- **11-model_state_insert.py**: Script that adds the `State` object “Louisiana” to the database `hbtn_0e_6_usa`.
- **12-model_state_update_id_2.py**: Script that changes the name of a `State` object from the database `hbtn_0e_6_usa`.
- **13-model_state_delete_a.py**: Script that deletes all `State` objects with a name containing the letter 'a' from the database `hbtn_0e_6_usa`.
- **14-model_city_fetch_by_state.py**: Script that lists all `City` objects from the database `hbtn_0e_14_usa`.
- **100-relationship_states_cities.py**: Script that creates the `State` “California” with the `City` “San Francisco” from the database `hbtn_0e_100_usa`.
- **101-relationship_states_cities_list.py**: Script that lists all `State` objects, and corresponding `City` objects, contained in the database `hbtn_0e_101_usa`.
- **102-relationship_cities_states_list.py**: Script that lists all `City` objects from the database `hbtn_0e_102_usa`.

## Models

- **model_state.py**: Contains the class definition of a `State` and an instance `Base = declarative_base()`.
- **model_city.py**: Contains the class definition of a `City`.
- **relationship_city.py**: Contains the class definition of a `City` with a relationship to the `State`.
- **relationship_state.py**: Contains the class definition of a `State` with a relationship to the `City`.

## Usage

Each script can be executed by using `python3` followed by the file name. For example:

```bash
$ python3 0-select_states.py
```

Make sure to have `MySQLdb` and `SQLAlchemy` installed and the database set up before running the scripts.

## Author

[Precious Amaechi]
