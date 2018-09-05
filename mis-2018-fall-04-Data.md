# IMSE 4410 Fall 2018 - Module 1

*IMSE 4410/7410 Management Information Systems Design (MIS)*

Material Copyright 2017, 2018 by Timothy Middelkoop. Sourcecode licensed under the Apache License, Version 2.0. Documentation licensed under CC by SA 3.0.

## Topic 4 - Engineering Data

"It's all data"

In Module 1 Topic 4 we will cover "data" in information technology systems and the different ways representing, managing, and using this data.

### Reading
* ISBB Chapter 4 - Data (https://bus206.pressbooks.com/chapter/chapter-4/)
* JSON data format and specification: http://www.json.org/


### Data

In order to collect, process, and analyze data we must first store and represent it in a computing and storage system.  Most data can be represented by the following fundamental data types (this is a loose definition):

 * Byte: an opaque 8-bit value. Often represented in hex.  Example `0xFF 0xFE`
 * Integer: A whole number (Int32, Int64). Example: `42`
 * Float: A floating point number (an estimate), (Float32, Float64).  Often represented in IEEE 754 format. Example `3.14e1`
 * String: Human readable text.  Often encoded as UTF-8. Example `"世界"`
 * Boolean: True or False
 * Array: An indexed collection of values. Index starts at 0 ('C' format) or 1 (Fortran format).  Example: `[ 100, 200, 300]`
 * Associative Array: A collection of key/value pairs.  Accessed via the key.  Example `{"Apple": 1, "Banana":2}`
 * Date and Time: Seconds since January 1, 1970. Often displayed in ISO 8610. Example: `2017-09-19T08:00Z`
 * Object.  A collection named attributes with values.
 * NULL: The absence of a value.

The data transfer format we will be using this semester
is [JSON](http://www.json.org/).  Example:
```JSON
{
	"Apple": 1,
	"Banana": 2,
	"Carrot": [100, 200, 300]
}
```

### Hands-On Python

[Python](http://python.org) is an popular Open Source language for
scripting and doing data processing.  In this class will be using
Python 3.

Log in to the teaching cluster for the following hands-on exercise.

First, Create a new file called `data.json` and place the above JSON
example in it.  Run the following test (`jq`) to ensure the data is formatted
correctly.

```bash
echo '{"Apple": 1, "Banana": 2, "Carrot": [100, 200, 300]}' > data.json 
jq . data.json
```

To start an interactive Python 3 shell on a node run the following command:
```bash
srun --pty python3
```

Then enter the following commands to load the JSON data.
```python
import json
f=open("data.json")
d=json.load(f)
f.close()
```

Show the data structure in Python
```
d
```

Add "Apples and Banana's"
```python
d["Apple"]+d["Banana"]
```

To exit Python either press the `control-d` key or run the exit function.
```python
exit()
```

### Homework
Homework 1-5: JSON and Python:
  1. In your class repository create a folder called `homework-1-5` and place all the files here.
  2. In this folder create a `example1.json` file with **valid** JSON that represents some data.  For example (but you cannot use this one) a sample from a weather station.
  3. Load this data into Python and do some simple calculations on it.  Feel free to read the Python manual for advanced commands.
  5. Copy the calculations and the results into a `output.md` file the homework folder (text, not screen-shots).
  4. Commit and push your work (the JSON and `output.md` file) to Gitlabs.
  6. Copy the `commit-id` and the repository URL


### References
* ASCII https://en.wikipedia.org/wiki/ASCII
* UTF-8/Unicode http://www.fileformat.info/info/charset/UTF-8/list.htm
* JSON data format and specification: http://www.json.org/
* Relational Databases http://www.tomjewett.com/dbdesign/
* SQL database SQLite: http://www.sqlite.org/
* SQLite tutorial: http://www.sqlitetutorial.net/
* Software Carpentry - Databases and SQL: http://swcarpentry.github.io/sql-novice-survey/

