# Make your code explicit

There should be no doubt when reading your code. There should be no black magic or surprises either. When a person reads your code it must be self-evident and as clear as possible as to its intent.

## No spreading

All your parameters and props should be explicitly listed. Do not spread your props.

Let us assume we pass the following props to our `Component`:

```
const user = {
    firstName: 'John',
    lastName: 'Doe'
};
```

❌ Bad

```
<Component {...user} />
```

😊 Good

```
<Component 
    firstName={firstName} 
    lastName={lastName} 
/>
```

_Why?_

We want to reduce the amount of work needed by the reader of the code to derive the intent.

In the first example we need to find where `user` is defined, and then understand what its members are to just then understand what is being passed into the `Component`. We then need to see if it is passing in more or less than what is expected.

In the second example, without having to leave where you are in the code, you can clearly see what the `Component` is taking.