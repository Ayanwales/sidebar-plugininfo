## Sidebar components
- Description
This list all the sidebar menus in the chat

    Endpoint : 
    ```sh 
    todo.zuri.chat/v1/ sidebar
    ```
    BaseUrl :
    ```sh
    https//todo.zuri.chat/api/v1
    ```
    Request Method: Get

- Parameter.

```sh
 Name                       Datatype                   Description 
 Organization_id            Integer                 Id of the organization 
 Plugin_id                  Integer                 Id of  the plugin 
User_id				        Integer		            Id of the user
Auth					    string			        Authorization header
```

- Responses

```sh
Code					Description
200	        			successful operation
```

Example:
```sh
{
  "name": "Todo Plugin",
  "description": "string",
  "plugin_id": "string",
  "organisation_id": "string",
  "user_id": "string",
  "group_name": "Tdo",
  "show_group": false,
  "joined_rooms": {
    "title": "Todo 2",
    "id": "string",
    "unread": null,
    "members": null,
    "icon": "string",
    "action": "open",
    "organisation_id": "string",
    "owner": "string",
    "user_id": "string"
  },
  "public_rooms": {
    "title": "Todo 2",
    "id": "string",
    "unread": null,
    "members": null,
    "icon": "string",
    "action": "open",
    "organisation_id": "string",
    "owner": "string",
    "user_id": "string"
  }
} 
```

```sh
Code					Description
400	                	invalid request
```

## Plugin information
- Description

 It gives information about new functions to host program without altering the host program itself. And it also keep the user within the program environment.
 
Endpoint :
```sh
todo.zuri.chat/v1/ info
```
BaseUrl :
```sh
https//todo.zuri.chat/api/v1
```
Request Method:Get

- Parameter 
```sh
Name					Datatype    		Description
Organization_id	        Integer	          	Id of the organization
Plugin_id				Integer  		    Id of  the plugin
User_id			    	integer	            Id of the user
Auth					string		    	Authorization header
```

- Responses

```sh
Code					Description
201			        	successful operation
```


Example:
```sh
 {
  "name": "string",
  "description": "string",
  "scaffold_structure": "Monolith",
  "ping_url": "https://todo.zuri.chat/api/ping",
  "html_url": "https://todo.zuri.chat/#/main",
  "sidebar_url": "https://todo.zuri.chat/api/sidebar"
}
```
```sh
Code					Description
400	                	invalid request
```