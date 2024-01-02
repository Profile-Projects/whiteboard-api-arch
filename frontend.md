# Front End Architecture

White board application needs to be esy to use on front end and should provide various tool to create with

Concurrent users should not feel any lag and functionalities should be ease of use.

## Global State

```
{
    active_users: [element_sid]
    users: {
        element_sid: {

        }
    },
    cursors: {
        element_sid: {
            x: "",
            y: ""
        }
    },
    active_elements: [element_sid],
    elements: [element_sid],

    element_position: {
        element_sid: {
            position: {

            },
            last_changed_user: element_sid,
            last_changed_timestamp: timestamp 
        }
    },

    element_size: {
        element_sid: {
            size: 5
        }
    },

    element_attr: {
        element_sid: {

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

