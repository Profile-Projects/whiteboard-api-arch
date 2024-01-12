# Front End Architecture

White board application needs to be esy to use on front end and should provide various tool to create with

Concurrent users should not feel any lag and functionalities should be ease of use.

## Global State

```
{
    board: {
        active: {
            name: "",
            description: "",
            sid: "",
            owner_sid: ""
        },
        all_board_sid: []
    },
    user: {
        active: {

        },
        board_users: [],
        cursors: {
            element_sid: {}
        }
    },
    elements: {
        element_sid: {
            position: {
                last_changed_user: user_sid,
                last_changed_timestamp: itimestamp
            },
            size: {
                last_changed_user: user_sid,
                last_changed_timestamp: itimestamp
            }
        }
    }

}

```


## User Action based hooks

```
    const elementPositionHook = ({ sid, position }) => {

        const [ position ] = useState(position);

        
        updateFromRemote = () => {

        }
        <!-- update in global state -->
        dispatch();

    }
```

