## Readings: CSS Transforms, Transitions, and Animations

### 8/19/22: Our reading today is based on CSS Transforms, Transitions, and Animations. 
---

## CSS Transforms

What does a CSS transform allow the developer to do to an element?
- **Transform** property allows an alternative way to size, position, and change elements. 
- It comes in a two-dimensional and three-dimensional setting. Each of these with their own individual properties and values. 
-  The actual syntax for the transform property is quite simple, including the transform property followed by the value. The value specifies the transform type followed by a specific amount inside parentheses.
- 2D:
- Scale, rotate, translate, skew
- It is common for multiple transforms to be used at once, rotating and scaling the size of an element at the same time for example. In this event multiple transforms can be combined together. To combine transforms, list the transform values within the transform property one after the other without the use of commas.

Provide an example of a transform and how you could see that being used on a website.
- You could use the 2D cube transform to create a cube like object for use in a game possibly. 

## CSS Transitions & Animations

What does a CSS transition allow the developer to do to an element?
- With CSS3 transitions you have the potential to alter the appearance and behavior of an element whenever a state change occurs, such as when it is hovered over, focused on, active, or targeted.
- As mentioned, for a transition to take place, an element must have a change in state, and different styles must be identified for each state. The easiest way for determining styles for different states is by using the `:hover, :focus, :active,` and `:target pseudo-classes`.
- There are four transition related properties in total, including `transition-property, transition-duration, transition-timing-function, and transition-delay.` Not all of these are required to build a transition, with the first three are the most popular.
- The transition-property property determines exactly what properties will be altered in conjunction with the other transitional properties. By default, all of the properties within an element’s different states will be altered upon change. However, only the properties identified within the transition-property value will be affected by any transitions.
- Duration, timing, delay 


How does a CSS animation differ from a CSS transition?
- When more control is required, transitions need to have multiple states. In return, this is where animations pick up where transitions leave off.
- To set multiple points at which an element should undergo a transition, use the `@keyframes` rule. The @keyframes rule includes the animation name, any animation breakpoints, and the properties intended to be animated.


## 8 Simple CSS3 Transitions 

What are some benefits to using CSS transitions on websites?
- Just a couple of lines of code will give you an awesome transition effect that will excite your users, increase engagement and ultimately, when used well, increase your conversions. What’s more, these effects are hardware accelerated, and a progressive enhancement that you can use right now.

How this topic fit in with your long-term goals?
- Great to understand how to customize your webpage in a way that engages your user. This will be important since I do enjoy designing webpages. 

[Back to main page](README.md)