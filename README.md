
---


#<center><img src="meteor.png">

---

<br>
##What Is Meteor?
Meteor is an open-source full-stack platform on which you can build web and mobile applications in Javascript. It is entirely real-time, which means any change to your database is automatically reflected live in the browser. It's also cross-platform, so you can use it on Andriod, iOS, and the Web. It can be integrated with MongoDB and depends on jQuery. It can also be used with any Javscript UI widget library. It has a Meteor CLI (command line interface) that can be used to create, build, and deploy applications, create and use packages, and update the framework. You can also use Meteor with Blaze, Angular, or React, as well as using Meteor for your whole stack by itself (though this is not a common practice anymore).

##Why Use Meteor?
Meteor allows you to develop your application in just one language.
Server-side and client side, for browser and mobile devices: everything is written in Javascript.

It sends *data* on the wire, not *HTML*. Therefore, the client renders the HTML.

It also follows the practice of React in seamlessly updating the user interface with current information from the server, except that Meteor is full-stack. Lag-time and latency become close to nonexistent. :party:


##Target Audience
Meteor is intended for developers who have at least some experience in Javascript and understand the general structure of the stack (front end vs. back end).


### Install on Mac: 
- Go to Terminal 
- Execute this comand:

``` bash
curl https://install.meteor.com/ | sh
```

### Install on Windows:
- Go to [Meteor Site](https://install.meteor.com/windows)

----
<br>

>Now that you have it... 

##How To Make Stuff in Meteor?

### Make a ToDo App: 
- [Angular & Meteor](https://www.meteor.com/tutorials/angular/creating-an-app)

- [Blaze & Meteor](https://www.meteor.com/tutorials/blaze/creating-an-app)

- [React & Meteor](https://www.meteor.com/tutorials/react/creating-an-app)

### Make a WhatsApp Clone
- [Angular & Meteor](https://angular-meteor.com/tutorials/whatsapp/meteor/bootstrapping)

##What Does It Look Like?
###React with Meteor:
Here's an example of a Task component:

```javascript
import React, { Component, PropTypes } from 'react';
 
// Task component - represents a single todo item
export default class Task extends Component {
  render() {
    return (
      <li>{this.props.task.text}</li>
    );
  }
}
 
Task.propTypes = {
  // This component gets the task to display through a React prop.
  // We can use propTypes to indicate it is required
  task: PropTypes.object.isRequired,
};
```
Here's an example of creating a tasks collection in React with Meteor:

```javascript
import { Mongo } from 'meteor/mongo';
 
export const Tasks = new Mongo.Collection('tasks');
```
#Review: Collections
Because Meteor uses MongoDB, you will encounter collections instead of tables. What are "collections"?

"Collections are Meteor's way of storing persistent data. The special thing about collections in Meteor is that they can be accessed from both the server and the client, making it easy to write view logic without having to write a lot of server code. They also update themselves automatically, so a view component backed by a collection will automatically display the most up-to-date data."
