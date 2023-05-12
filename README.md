![Screenshot (4)](https://github.com/Persie-O/AirBnB_clone/assets/112958325/efeff8e2-501b-478c-8bd5-c0fe4a3d758c)
                                        An AirBnB clone. 
![pipeline](https://github.com/Persie-O/AirBnB_clone/assets/112958325/e0c13815-40d8-4cf4-9af5-77a864b17c3f)
# Description 🏠
hbnb is a complete web application, integrating database storage, a back-end API, and front-end interfacing in a clone of AirBnB.

The project currently only implements the back-end console.

## Classes 🆑
hbnb utilizes the following classes:

|               | BaseModel   | FileStorage | User    | State | City  | Amenity  | Place | Review |
| :------------ |:-----------:|:-----------:|:-------:|:-----:|:-----:|:--------:|:-----:|:------:|
| PUBLIC INSTANCE ATTRIBUTES | `id` `created_at` `updated_at` | | Inherits from `BaseModel` | Inherits from `BaseModel` | Inherits from `BaseModel` | Inherits from `BaseModel` | Inherits from `BaseModel` | Inherits from `BaseModel` |
| PUBLIC INSTANCE METHODS | `save` `to_dict` | `all` `new` `save` `reload` | "" | "" | "" | "" | "" | "" |
| PUBLIC CLASS ATTRIBUTES | | | `email` `password` `first_name` `last_name` | `name` | `state_id` `name` | `name` | `city_id` `user_id``name` `description` `number_rooms` `number_bathrooms` `max_guest` `price_by_night` `latitude` `longitude` `amenity_ids` | `place_id` `user_id` `text` |
| PRIVATE CLASS ATTRIBUTES | | `file_path` `objects` | | | | | | |

## Storage 🛄
The above classes are handled by the abstracted storage engine defined in the FileStorage class.

Every time the backend is initialized, hbnb instantiates an instance of `FileStorage` called `storage`. The `storage` object is loaded/re-loaded from any class instances stored in the JSON file `file.json`. As class instances are created, updated, or deleted, the `storage` object is used to register corresponding changes in the `file.json`.

## Console 💻
The console is a command line interpreter that permits management of the backend of hbnb. It can be used to handle and manipulate all classes utilized by the application (achieved by calls on the `storage` object defined above).
