# react-quiz

# Please slack your local instructor the answers to these questions. 

## 1. Describe what .bind .call .apply do? 

## 2. Traditionally in web development, user input is stored in the DOM, and the data (e.g. what the user typed in the input field) is extracted from the DOM to use in the application logic. React dramatically simplifies input handling by treating input elements as stateless; an input element has a value prop and an onChange prop, and together these things give you total control over the input without ever having to touch the DOM.

## In your own words - describe/summarize what is happening in this component? 

``` import React, { Component } from 'react'
import { render } from 'react-dom'

class Input extends Component {

  state = {value: ''}

  handleChange = (e) => {
    this.setState({value: e.target.value})
  }

  render() {
    const {value} = this.state

    return (
      <div>
        <label htmlFor={'id'}>
          Enter value
        </label>
        <input
          id={'id'}
          type={'text'}
          value={value}
          placeholder={'Placeholder'}
          onChange={this.handleChange}
        />
        <br />
        <br />
        My value: {value}
      </div>
    )
  }
}

render(<Input />, document.querySelector('#app'))

```
## Every time we render the input, we pass the current value from our component's state. Every time the user types in the input field, we update state to include the new value, which triggers a re-render. This essentially keeps the DOM synced up to our component state automatically. We can control the value of the input field however we'd like, while React handles the DOM operations for us behind the scenes.

## 3. What is a controlled input in React? 

## 4. In  your own words, describe what setState() is  

## 5. Accessibilty is very important in web development - please take some time to read through this link and have a discusion amongst your classmates 
https://reactjs.org/docs/accessibility.html


