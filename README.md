# whiteboard-api-arch
Architecture for designing white board

## Functional Requirement

### Core Functionality

- Board Management: 
    * Create, name and organize multiple boards
    * Resize and reposition elements on board
    * zoom in/out detailed view

- User Management
    * Create user accounts with roles and permissions
    * Invite collaborators to board
    * Set access control(view, edit, comment)

- Drawing Tools
    * Shapes: Lines, rectangle, square, circle, freehand
    * Text box with styles
    * Sticky notes
    * Images and attachments

- Real-Time Collaboration
    * Concurrent users editing whiteboard
    * Cursor position visibility for collaborators
    * Instant updates and syncronization

### Additional Features

- Version History
    * Track changes made on the board
    * Revert to previous changes

- Export Options
    * Save as image(PNG, JPG)
    * Export as PDF
    * Generate sharable link

## Non Functional Requirement

- Performance
    * Low latency for real time collaboration
    * Fast load times for larger boards
    * Smooth rendering and panning

- Security
    * Data encryption for sensitive data
    * User authentication and authorization
    * Secure sharing and access control

- Usability
    * Intuitive interface and control
    * Clear visual feedbacks and cues
    * Accessibility features for users with disabilities

- Reliability
    * Stable performance under heavy usage
    * Data loss prevention and recovery
    * Regular updates and maintenance



# Services

## Board Service (**Spring Boot Application**)

API functionalities

### Board API

- Create new Board
- Edit Board Attributes (only meta data, not elements information)
- delete board

### User API
- Create new User
- Edit User information
- invite new user to board (signup and add to board)
- invite existing user to board
- User accepts invitation to join board


## Board Elements Service (**NodeJS Application**)

### WebSocket Functionalities

#### Add Element
- Add new element to board

#### Update Element
- Update element on board

#### Delete Element
- Delete element on board

#### Update User Cursor
- User cursor on the board update

#### Undo Element Action
- User specific undo action on board

#### Redo Element Action
- User specific redo action on board


### Operational Transform

Algorithm to identify changes required on board elements based on concurrent actions





