# Frontend Mentor - Stats preview card component solution

This is a solution to the [Stats preview card component challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/stats-preview-card-component-8JqbgoU62). Frontend Mentor challenges help you improve your coding skills by building realistic projects.

## Table of contents

- [Overview](#overview)
  - [The challenge](#the-challenge)
  - [Screenshot](#screenshot)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
  - [Continued Development](#continued-development)
  - [Useful resources](#useful-resources)
- [Author](#author)

## Overview

### The challenge

Users should be able to:

- View the optimal layout depending on their device's screen size

### Screenshot

![](./screenshot.jpg)

### Links

- Github Repo URL: [Stats Preview Card Repo](https://github.com/amyspencerproject/stats-preview-card)
- Live Site URL: [Stats Preview Card Page](https://amyspencerproject.github.io/stats-preview-card/)

## My process

### Built with

- Semantic HTML5 markup
- CSS Variables
- CSS Flex
- Mobile-first workflow

### What I learned

- Decided on CSS Flex layout for this challenge
- Took into consideration that this code would just be a component and not a stand alone page. Apllied styles to classes that could be easily copied and re-used in already established code for a page or app.
- Used letter-spacing to on the stat category text. Used rem units for this and did consider what will happen if someone increases the font size for accessiblity. Thought maybe it would be better to use a fixed px spacing unti. However the rem was so small it didn't seem to matter if I used px instead when I tested it out.
- Getting the image with the violet overlay was not straight forward for me. First I tried to set the image as a background image and then add a color gradient over it. To get this to work I had to specify the height of the background area in px. That is not good CSS practice.
- If the image in a `<img>` or `<picture>` div then it will take up the room it needs without me having to adjust for the height. I just need to figure out how to add the violet color. Maybe I can have a solid color background and then change the opacity of the image??
- Used an opacity of 40% to get a violet overlay on the image. It is not the same contrast/intensity as the image in the Figma file but it is fairly close.
- The desktop image does not cover the height of the card container between the viewport range of 960px to 1060px. The image is just shorter than what the rest of the elements are sizing at for that range. I played around with fixing the height of the card container but the image resized to be smaller during the same viewport range and then even beyond to about 1090px. I tried changing the media query for the image to 1060px but again it resized to stay small even with the taller image of 480px. Something is keeping a ratio but I do not understand this behavior.

  - media query and picture media query at 60rem or 960px
  - desktop size image is 540px x 446px
  - mobile size image is 654px x 480px

- Reached out on FEM's Discord and got this bomber answer!
  ![](./Screenshot-FEM-discord-help.png)

  There is no way I would have found this `align-items: center` issue. I was too far down the rabbit hole. This is why it is important to work in a team!

- Another FEM member told me to use `mix-blend-mode: multiply` to get much better intensity on the image overlay. Worked great!

### Continued development

### Useful resources

- [Letter Spacing](https://developer.mozilla.org/en-US/docs/Web/CSS/letter-spacing)
- [Picture element](https://www.w3schools.com/html/html_images_picture.asp)
- [Mix-blend mode](https://developer.mozilla.org/en-US/docs/Web/CSS/mix-blend-mode) - There is a way to further modify images in CSS!!

## Author

- Website - [Amy Spencer](https://spencerproject.com/)
- Frontend Mentor - [@amyspencerproject](https://www.frontendmentor.io/profile/amyspencerproject)
- Linkedin - [amyspencercodes](https://www.linkedin.com/in/amyspencercodes/)
