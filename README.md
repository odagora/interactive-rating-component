# Frontend Mentor - Interactive rating component solution

This is a solution to the [Interactive rating component challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/interactive-rating-component-koxpeBUmI). Frontend Mentor challenges help you improve your coding skills by building realistic projects.

## Table of contents

- [Overview](#overview)
  - [The challenge](#the-challenge)
  - [Screenshot](#screenshot)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
  - [Continued development](#continued-development)
  - [Useful resources](#useful-resources)
- [Author](#author)
- [Acknowledgments](#acknowledgments)

## Overview

### The challenge

Users should be able to:

- View the optimal layout for the app depending on their device's screen size
- See hover states for all interactive elements on the page
- Select and submit a number rating
- See the "Thank you" card state after submitting a rating

### Screenshot

![Rating Card Side](https://bit.ly/3cUKYLH)
![Message Card Side](https://bit.ly/3RKBrW2)
![Animation Card](https://res.cloudinary.com/dagrstwwf/image/upload/v1662678837/2022-09-08_18-13-22_ix2ags.gif)

### Links

- Solution URL: [Click here](https://bit.ly/3D7e7xL)
- Live Site URL: [Click here](https://bit.ly/3B53gBG)

## My process

### Built with

- Semantic HTML5 markup
- CSS custom properties
- Sass preprocessor
- Flexbox
- CSS Grid
- Mobile-first workflow
- BEM methodology

### What I learned
* Pixel perfect layout technique based on an image (without Figma design)

* Use of `form` `radio` button inputs for one choice selection

* Form `input` `radio` buttons custom styling from `label` html tag
```scss
& input {
    opacity: 0;
    position: fixed;
    width: 0;
    &:checked + label {
        @include radio-state($white, $orange);
    }
}

```

* Use of Sass Mixins
```scss
@mixin title-format {
    font-size: 2.5rem;
    font-family: $font;
    font-weight: 400;
    color: $white;
}
```
* Use of Sass Mixins with parameters
```scss
@mixin radio-state ($color, $background) {
    color: $color;
    background-color: $background;
}
```
* Use of vanilla JavaScript event listeners to manage component state
```js
form.addEventListener('submit', (e) => {
    e.preventDefault();
    const rating = document.querySelector('input[name="rating"]:checked').value;

    ratingTag.innerText = `You selected ${rating} out of 5`;
    cardRating.style.display = 'none';
    cardMessage.style.display = 'block';
})
```
### Continued development

* Use of preprocessors like SASS for styling
* Use of CSS Grid in complex layouts
* Use of transformations and animations with CSS
* Use of JavaScript for DOM manipulation and interactivity

### Useful resources

- [PixelParalell Chrome Extension](https://bit.ly/3B04jTG) - This helped me for applying Pixel Perfect Layout technique. I really liked this extension and will use it going forward.
- [Customize radio button appearance with css](https://markheath.net/post/customize-radio-button-css) - This is an amazing post which helped me style form radio buttons with custom css properties.

## Author

- Website - [Daniel González](https://odagora.com)
- Frontend Mentor - [@odagora](https://www.frontendmentor.io/profile/odagora)
- Twitter - [@odagora](https://www.twitter.com/odagora)

## Acknowledgments

The Frontend Platzi courses helped me with the basic concepts of semantic HTML, CSS3 and BEM methodology. Also, I implemented best practices regarding responsive design, performance and accesibility.
