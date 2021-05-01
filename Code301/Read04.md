1. What is a ‘Controlled Component’?

A controlled component is a react component that controls the values of input elements in a form using setState().

2. Should we wait to store the users responses from the form into state when they submit the form OR should we update the state with their responses as soon as they enter them? Why.

we should update the state with their responeses as soon as they enter them because the React take some time to update the state so if we did this after the submition maybe anonther compenent depends on these values will not work propely.

3. How do we target what the user is entering if we have an event handler on an input field?

by using the `event.target.name` for that input filed.

# React and Forms

## Form

### Controlled Components

In HTML, form elements such as `<input>, <textarea>, and <select>` typically maintain their own state and update it based on user input. In React, mutable state is typically kept in the state property of components, and only updated with setState().

We can combine the two by making the React state be the “single source of truth”. Then the React component that renders a form also controls what happens in that form on subsequent user input. An input form element whose value is controlled by React in this way is called a “controlled component”.

### The textarea Tag

In HTML, a `<textarea>` element defines its text by its children:

In React, a `<textarea>` uses a value attribute instead. This way, a form using a `<textarea>` can be written very similarly to a form that uses a single-line input.

### The select Tag

In HTML, `<select>` creates a drop-down list. For example, this HTML creates a drop-down list of flavors:

```javascript
<select>
   <option value="lime">Lime</option>
   <option selected value="coconut">Coconut</option>
   <option value="mango">Mango</option>
></select>
```

Note that the Coconut option is initially selected, because of the selected attribute. React, instead of using this selected attribute, uses a value attribute on the root select tag. This is more convenient in a controlled component because you only need to update it in one place. For example:

```javascript
class FlavorForm extends React.Component {
  constructor(props) {
    super(props);
    this.state = {value: 'coconut'};

    this.handleChange = this.handleChange.bind(this);
    this.handleSubmit = this.handleSubmit.bind(this);
  }

  handleChange(event) {
    this.setState({value: event.target.value});
  }

  handleSubmit(event) {
    alert('Your favorite flavor is: ' + this.state.value);
    event.preventDefault();
  }

  render() {
    return (
      <form onSubmit={this.handleSubmit}>
        <label>
          Pick your favorite flavor:
          <select value={this.state.value} onChange={this.handleChange}>
            <option value="grapefruit">Grapefruit</option>
            <option value="lime">Lime</option>
            <option value="coconut">Coconut</option>
            <option value="mango">Mango</option>
          </select>
        </label>
        <input type="submit" value="Submit" />
      </form>
    );
  }
}
```

Overall, this makes it so that `<input type="text">, <textarea>`, and `<select>` all work very similarly - they all accept a value attribute that you can use to implement a controlled component.

### The file input Tag

In HTML, an `<input type="file">` lets the user choose one or more files from their device storage to be uploaded to a server or manipulated by JavaScript via the File API.

```javascript
<input type="file" />
```

Because its value is read-only, it is an uncontrolled component in React.

### Handling Multiple Inputs

When you need to handle multiple controlled input elements, you can add a name attribute to each element and let the handler function choose what to do based on the value of event.target.name.

For example:

```javascript
class Reservation extends React.Component {
  constructor(props) {
    super(props);
    this.state = {
      isGoing: true,
      numberOfGuests: 2
    };

    this.handleInputChange = this.handleInputChange.bind(this);
  }

  handleInputChange(event) {
    const target = event.target;
    const value = target.type === 'checkbox' ? target.checked : target.value;
    const name = target.name;

    this.setState({
      [name]: value
    });
  }

  render() {
    return (
      <form>
        <label>
          Is going:
          <input
            name="isGoing"
            type="checkbox"
            checked={this.state.isGoing}
            onChange={this.handleInputChange} />
        </label>
        <br />
        <label>
          Number of guests:
          <input
            name="numberOfGuests"
            type="number"
            value={this.state.numberOfGuests}
            onChange={this.handleInputChange} />
        </label>
      </form>
    );
  }
}
```

## The Conditional (Ternary) Operator

### Starting With the Basics — The if statement

Using a conditional, like an `if` statement, allows us to specify that a certain block of code should be executed if a certain condition is met.

but you can do the same exact thing only in one line using the conditional ternaty operator:

```javascript
condition ? value if true : value if false
```

Here’s what you need to know:

1. The `condition` is what you’re actually testing. The result of your condition should be `true` or `false` or at least coerce to either boolean value.

2. A `?` separates our conditional from our true value. Anything between the `?`and the `:` is what is executed `if` the `condition` evaluates to `true`.

3. Finally a `:` colon. If your condition evaluates to `false`, any code after the colon is executed.
