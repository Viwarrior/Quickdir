# Quickdir
JSON object to quick directory creator using python.

## Installation

Clone the repository and import Quickdir.py file.

## Usage

In Json object structure, terminating values has to be supplied to end(leaf) nodes in dir structure. Supply 1 if it ends with a file, 0 if it ends with a folder.

```json
json = {"folder": {
                "subfolder": {
                        "subsubfolder": 0,
                        "file.txt": 1
                    }
         }

```

Creating dir using Quickdir object
```python
import Quickdir

# only if using config.json
import config

# create object of Quickdir class 
quick = Quickdir("Quickdir")

# give custom path instead of 'Quickdir' if required
quick2 = Quickdir("S:/Files")

# Create and pass your json object or edit config.json in config.py
quick.make(config.json2)
```

## Applications
Example 1: HTML project
```python
json = {"root": {
                "logs": {
                        "test": 0,
                        "log.txt": 1
                    },
                "css" : {
                        "style.css" : 1,
                        "bootstrap.css": 1
                    },
                "js": {
                        "mainFunction.js":1,
                        "bootstrap.js":1,
                        "jquery.js":1
                    },
                "common":{
                        "navbar.html" :1,
                        "footer.html" :1
                    },
                "Readme.md": 1,
                "fonts": {
                    "sample.txt" :1
                  },
                "img": 0,
                "index.html":1
                
        } 
    }

```


Example 2: Creating directory structure for a College course.
```python
json2 = {"CSE420": {
                "cat1": {
                        "alternate material": 0,
                        "notes.txt": 1
                    },
                "cat2": {
                        "alternate material": 0,
                        "notes.txt": 1
                    },
                "lab" : {
                        "1":0,
                        "2":0, 
                        "3":0,
                        "4":0,
                        "5":0,
                        "midterm":0,
                        "labfat":0,
                        "notes.txt": 1
                    },
                "DA": {
                        "1":0,
                        "2":0
                    },
                "FAT":{
                        "notes.txt" :1
                    },
                "project": {
                        "review 1": 0,
                        "review 2": 0,
                        "review 3": 0,
                        "code": {
                                  "test.py":1  
                        }
                    },
                
                "syllabus": 0
                
        } 
    }
```

## Contributing
Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.


## License
[MIT](https://choosealicense.com/licenses/mit/)
