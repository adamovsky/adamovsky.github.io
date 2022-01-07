# Philosophy

The overarching philosophy is: _simplicity over complexity_.

Here we break down what that means.

## Single purpose

Everything should focus on doing one thing and do that one thing well. 

This includes everything including functions, components, stories, tasks.

### User Stories

As soon as a story has a binary operator (e.g. "and", "or") in the requirement, that is a good place to break down the story into either smaller stories or tasks.

❌ Bad

```
User Story: As a user I want the component to do X, Y, and Z
```

😊 Good

```
User Story: As a user I want the component to do X
User Story: As a user I want the component to do Y
User Story: As a user I want the component to do Z
```

_Why?_

An engineer can solve a simple problem faster than a complex problem.

A complex problem doing one thing is still simpler than a complex problem doing many things.

Having a story do one thing can be released faster, and therefore value can be added to the business more incrementally.

In the above example, value can be added in increments of 33% over time. This gives business more opportunity to course correct with each iteration.

Having one big story released in one big bang requires it to be delivered all at once.  This gives business zero opportunity to course correct an implementation and needs to be sent back and redone in case of misalignment.

## Decompose complexity into individual simple parts

When your component returns markup, it should have minimal HTML tags (e.g. `div`, `span`, `p`). There should be more custom elements (e.g. components) in the code.  

The more HTML tags a component returns, the more opportunities there are for decomposing the component further.

❌ Bad

```
<div>
    <span>
        Some Title
    </span>

    <p>
        Some latin text goes here
    </p>

    <img src="image.jpg" />
</div>
```

😊 Good

```
<div>
   <Title text="Some Title" />

   <BodyText text="Some latin text goes here" />

   <ResponsiveImage image="image.jpg" />
</div>
```