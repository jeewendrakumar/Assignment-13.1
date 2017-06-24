React.Component
Components let you split the UI into independent, reusable pieces, and think about each piece in isolation. React.Component is provided by React.

Overview
React.Component is an abstract base class, so it rarely makes sense to refer to React.Component directly. Instead, you will typically subclass it, and define at least a render() method.

Normally you would define a React component as a plain JavaScript class:

class Greeting extends React.Component {
  render() {
    return <h1>Hello, {this.props.name}</h1>;
  }
}
If you don't use ES6 yet, you may use the create-react-class module instead. Take a look at Using React without ES6 to learn more.

The Component Lifecycle
Each component has several "lifecycle methods" that you can override to run code at particular times in the process. Methods prefixed with will are called right before something happens, and methods prefixed with did are called right after something happens.

Mounting
These methods are called when an instance of a component is being created and inserted into the DOM:

constructor()
componentWillMount()
render()
componentDidMount()
Updating
An update can be caused by changes to props or state. These methods are called when a component is being re-rendered:

componentWillReceiveProps()
shouldComponentUpdate()
componentWillUpdate()
render()
componentDidUpdate()
Unmounting
This method is called when a component is being removed from the DOM:

componentWillUnmount()


RelayContainer

RelayContainer is a higher-order React component that lets a React component encode its data requirements.

Relay ensures that this data is available before the component is rendered.
Relay updates the component whenever the underlying data has changed.
Relay containers are created using Relay.createContainer.
