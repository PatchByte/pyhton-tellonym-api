# Tellonym API

# Creating the API
```python
import tellonym_api

api = tellonym_api.TellonymApi()
```
------
# How to check if a user exists!
```python
import tellonym_api

api = tellonym_api.TellonymApi()

user = api.GetUser("[your user]")
if user.IsProfileFound() == True:
    #profile is existing
else:
    #profile isnt existing!
```
------
# Simple User Getter
```python
import tellonym_api

api = tellonym_api.TellonymApi()
user = api.GetUser("[user]")
if not user.IsProfileFound() == True:
    exit("Profile isnt existing!")

user.FetchFollowers()
user.FetchFollowings()
user.FetchTells()

print(user.GetTells())
print(user.GetFollowers())
print(user.GetFollowings())
```


> Made with <3 by PatchByte
# And a **BIG** thank you to piotrusieeeek
