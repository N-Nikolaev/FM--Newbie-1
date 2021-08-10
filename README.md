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
  - [Continued development](#continued-development)
  - [Useful resources](#useful-resources)
- [Author](#author)
- [Acknowledgments](#acknowledgments)

**Note: Delete this note and update the table of contents based on what sections you keep.**

## Overview

### The challenge

Users should be able to:

- View the optimal layout depending on their device's screen size

### Screenshot

**Desktop View**

![](src/design/screenshot-desktop.png)

**Mobile View**

![](src/design/screenshot-mobile.png)

### Links

- Solution URL: [Github Repository](https://github.com/N-Nikolaev/FM--Newbie-1)
- Live Site URL: [Github Page](https://n-nikolaev.github.io/FM--Newbie-1)

## My process

### Built with

- Semantic HTML5 markup
- CSS custom properties
- CSS Grid
- Mobile-first workflow
- [SASS](https://sass-lang.com/) - CSS Preprocessor
- [Parcel](https://parceljs.org/) - Web Application Bundler


### What I learned

Through this project I was able to learn how to set-up Parcel in order to process my SASS code and bundle everything for distribution. 

```json
"scripts": {
  "dev": "parcel src/index.html",
  "build": "parcel build src/index.html"
}
```

In addition to learning how to be more comfortable with the SASS syntax, I was both able to make create and use media query mixins, as well as use CSS Grid to control the layout of the component. 

```scss
// Media Query Mixin
@mixin mq {
  @media (min-width: $br--laptop) {
    @content;
  }
}

.card {
  display: grid;
  grid-template-areas: 
    "img"
    "content";

  @include mq {
    grid-template-areas: 
      "content img";
  }
}
```

And finally, I was able to find a simple and elegant way in order to blend an image without having to create an overlay element.

```scss
img {
  mix-blend-mode: multiply;
  opacity: 0.8;
}
```


### Continued development

Moving forward, I have decided to focus on using CSS Grid over Flexbox whenever possible. It has come to light through this project that I struggle when it comes to using Grid to solve problems in which I would usually resort to Flexbox. 

Additionally, I will be trying to figure out how to properly use GIT, especially subtrees. As a beginner with GIT I have often times found myself having to recreate my gh-pages repository. I have acknowledge my lack basic knowledge of GIT commands and my tenuous grasp on the process of version control to be hindering me. 


### Useful resources

- [Code Guide by @mdo](https://codeguide.co/) - This was useful when it came to cleanly structuring my SASS code and made it much easier for me to take in what I was writing. I am a big fan of this code guide and will be using it to structure my code in the future. 

- [Deploying a subfolder to GitHub Pages](https://gist.github.com/cobyism/4730490) - This was helpful when I needed to find a way to set-up a Github page for my project. Parcel doesn't allow for output directory naming (as far as I know) and so I had to find a work around. I will be using the method outlined inside until I can find a way to serve my GH page form the main repo. 

- [SASS + Parcel Set-up ](https://www.youtube.com/watch?v=wYWf2m_yzBQ) - This video by Kevin Powell is what I followed in order to set up both SASS and Parcel together. I highly recommend it to anyone who wants to dip their toes into Parcel.


## Author

- Github - [Nikolay Nikolaev](https://github.com/N-Nikolaev)
- Frontend Mentor - [@N-Nikolaev](https://www.frontendmentor.io/profile/N-Nikolaev)


## Acknowledgments

I'd like to thank Kevin Powell for his video on ["Escaping Tutorial Hell"](https://youtu.be/QqDH5sYzDS8) (something I've been meaning to do for a long time now) and for his many other tutorial videos which were indispensible to me during the course of this project.

