## Categories
- file system

## Query
find all text files in the current directory and move them to tmp

## Query code
```
move(
    find_all(type=TextFile, inside=get_current_directory()),
    '/tmp',
)
```

## Thoughts

1. agent can use next pattern:  
function is being called with a list of objects instead of one object, but type is expected.  
this means that we need to call this function for every object in list  

2. "current directory" refers to an idea of "CurrentDirectory", so we need to look for collocations and map them to known ideas (concepts).  
after we found that "current directory" = "CurrentDirectory" agent is looking for a way to get current directory, function get_current_directory returns it, so agent uses it.  
