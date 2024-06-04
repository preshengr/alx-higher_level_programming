# 0x14-javascript-web_scraping

## Introduction

This repository contains JavaScript scripts that demonstrate how to perform web scraping, interact with web APIs, and manipulate data from external sources using Node.js.

## Scripts

### 0-readme.js

**Usage:**
```
$ node 0-readme.js
```

**Description:**
This script reads the content of a specified file and prints it to the standard output (console).

**Usage:**
- Replace `<file_path>` with the path to the file you want to read.

### 1-writeme.js

**Usage:**
```
$ node 1-writeme.js <file_path> <content>
```

**Description:**
This script writes the specified content to a specified file.

**Parameters:**
- `<file_path>`: The path to the file you want to write to.
- `<content>`: The content you want to write to the file.

### 100-starwars_characters.js

**Usage:**
```
$ node 100-starwars_characters.js <film_id>
```

**Description:**
This script retrieves and prints the names of characters appearing in a specified Star Wars film. It fetches data from the Star Wars API (https://swapi.dev/).

**Parameters:**
- `<film_id>`: The numerical ID of the Star Wars film whose characters you want to retrieve.

### 101-starwars_characters.js

**Usage:**
```
$ node 101-starwars_characters.js <film_id>
```

**Description:**
This script retrieves and prints the names of characters appearing in a specified Star Wars film. It fetches data from the Star Wars API (https://swapi.dev/). This script uses asynchronous functions and `axios` library for making HTTP requests.

**Parameters:**
- `<film_id>`: The numerical ID of the Star Wars film whose characters you want to retrieve.

### 2-statuscode.js

**Usage:**
```
$ node 2-statuscode.js <URL>
```

**Description:**
This script sends a GET request to a specified URL and prints the status code of the response.

**Parameters:**
- `<URL>`: The URL to which you want to send the GET request.

### 3-starwars_title.js

**Usage:**
```
$ node 3-starwars_title.js <film_id>
```

**Description:**
This script retrieves and prints the title of a specified Star Wars film. It fetches data from the Star Wars API (https://swapi.dev/).

**Parameters:**
- `<film_id>`: The numerical ID of the Star Wars film whose title you want to retrieve.

### 4-starwars_count.js

**Usage:**
```
$ node 4-starwars_count.js
```

**Description:**
This script retrieves and prints the number of films in which the character "Wedge Antilles" appears. It fetches data from the Star Wars API (https://swapi.dev/).

### 5-request_store.js

**Usage:**
```
$ node 5-request_store.js <URL> <file_path>
```

**Description:**
This script sends a GET request to a specified URL, retrieves the response body, and writes it to a specified file.

**Parameters:**
- `<URL>`: The URL from which you want to retrieve the response body.
- `<file_path>`: The path to the file where you want to save the response body.

### 6-completed_tasks.js

**Usage:**
```
$ node 6-completed_tasks.js <URL>
```

**Description:**
This script retrieves a list of completed tasks from a specified URL and prints the number of tasks completed by each user.

**Parameters:**
- `<URL>`: The URL from which you want to retrieve the list of completed tasks.

## License

Licensed to ALX - Holberton School

## Authors

- Precious Okwukwe Amaechi
