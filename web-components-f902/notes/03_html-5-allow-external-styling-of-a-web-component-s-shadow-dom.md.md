# Allow External Styling of a Web Component's Shadow DOM

[Video link](https://egghead.io/lessons/html-5-allow-external-styling-of-a-web-component-s-shadow-dom)

<TimeStamp start="1:05" end="1:15">

The first way to allow external styling of a web component's shadow DOM is to add a method (`changeStyle(styles)`) in our `CustomElement` class.

</TimeStamp>

<TimeStamp start="1:36" end="1:41">

In the console: `$0.changeStyles`

</TimeStamp>

<TimeStamp start="1:42" end="1:50">

In the console: `$0.changeStyles({color: 'red'})`

</TimeStamp>

<TimeStamp start="1:51" end="2:00">

In the console: `$0.changeStyles({color: 'red', textDecoration: 'underline'})`

</TimeStamp>

<TimeStamp start="2:24" end="2:34">

`attributeChangedCallback()` works in conjunction with our getter method, `observedAttributes()`, by firing anytime a custom element's attributes is modified

</TimeStamp>

<TimeStamp start="3:12" end="3:19">

In the console: `$0.setAttribute('color', 'purple')`

</TimeStamp>
