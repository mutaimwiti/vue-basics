**Vue Basics**

This is a step by step `vuejs` introductory tutorial. This 
file is updated on each revision. 

Before going too far install the [Vue Devtools](https://github.com/vuejs/vue-devtools#vue-devtools).
This allows you to inspect and debug vue applications more easily than basic browser
consoles.

#####Lesson 1

The first thing you learn about Vue is the two way data binding.

```
<div id="app">
    Say something: <input v-model="message">

    <p>You said: {{ message }}</p>
</div>

new Vue({
    el: '#app',
    data: {
        message: 'Nothing yet'
    }
})
```
######Let's focus on the javascript.

`new Vue` creates a new vuejs instance. You are not tied down to one on per view.

`el` is the point where the Vue instance is mounted. It defines the operating 
boundaries of the vue instance. The instance has effects only on the elements 
within the element where vue is mounted.

`data` is where you place the data of your instance. It is the single source of 
truth for the instance. You are not limited on the number of data elements that
your instance can use.

######Back to the html.

`<div id="app">` is the element that contains our vue instance. It is where our 
instance is mounted.

`v-model="message"` creates a binding between the input element and the data on the 
vue instance. This means that when the input is updated the data is updated. The 
input is also happens when the data is updated. This is two way data binding.

`<p>You said: {{ message }}</p>` always displays the most recent message. It is very
reactive to any changes occurring on message. This is reactivity and in vue it 
happens at lighting fast speeds. I'm trying to say that updates are applied at 
the blink of an eye.

`{{ }} - Moustash syantax` is used to echo out data on vue. It is very simple and
straightforward saving you many keystrokes.