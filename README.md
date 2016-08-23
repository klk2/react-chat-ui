# react-chat-ui
A library of React components for building chat UI's.

### !!Use at own risk!!
This project is still in the VERY early stages of development. If you encounter a bug or have a feature request, please create an issue and/or tweet at me [here](http://twitter.com/brandonmowat).


![react-chat-ui logo](https://i.imgur.com/YhPrFWw.png)

### Installation
`npm install react-chat-ui`

### Basic Usage
```javascript
import { ChatFeed } from 'react-chat-ui'

// Your code stuff...

render() {

  return (

    // Your JSX...

    <ChatFeed
      messages={this.state.messages} // Boolean: list of message objects
      is_typing={this.state.is_typing} // Boolean: is the recipient typing
      bubbleStyles={{ // JSON: Custom bubble styles
        text: {
          fontSize: 30,
        },
        chatbubble: {
          borderRadius: 70,
          padding: 40,
        }
      }}
    />

    // Your JSX...

  )

}
```

Make sure to keep a list of proper message objects in your class state.
Like so:
```javascript

//...
this.state = {
  messages : [
    {type:1, message: "I'm the recipient! (The person you're talking to)"}, // Gray bubble
    {type:0, message: "I'm the user!"}, // Blue bubble
  ],
  //...
}
//...

```