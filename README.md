# Frontend Mentor - Product preview card component solution

This is a solution to the [Product preview card component challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/product-preview-card-component-GO7UmttRfa). Frontend Mentor challenges help you improve your coding skills by building realistic projects. 

## Table of contents

- [Overview](#overview)
  - [Screenshot](#screenshot)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
- [Author](#author)

## Overview

### Screenshot

![Screenshot 2023-05-07 at 12 11 09](https://user-images.githubusercontent.com/69512496/236671339-6df51633-3aef-44cc-a60c-b7975c0ae278.png)

### Links

- Solution URL: https://github.com/hassanidris/product-preview-card-component-main
- Live Site URL: https://hassanidris.github.io/product-preview-card-component-main/

## My process

### Built with

- SASS / CSS Variables
- Semantic HTML5 markup
- CSS custom properties
- Flexbox
- CSS Grid
- Mobile-first workflow

**Note: These are just examples. Delete this note and replace the list above with your own choices**

### What I learned

To see how you can add code snippets, see below:

- CSS Variables

```scss
 --clr-darkCyan-prm-400: hsl(158, 36%, 37%);
 --clr-darkCyan-prm-hover: hsl(158, 36%, 20%);
 --clr-cream-prm-200: hsl(30, 38%, 92%);
```

- Nesting media queries inside the classes

```scss
.product {
    --content-padding: 1.5rem;
    --content-spacing: 1rem;

    display: grid;
    background-color: var(--white-nut-100);
    border-radius: 0.5rem;
    overflow: hidden;
    max-width: 600px;

    @media (min-width: 650px) {
        --content-padding: 2rem;
        grid-template-columns: 1fr 1fr;
    }

    &__content {
        display: grid;
        gap: var(--content-spacing);
        padding: var(--content-padding);
    }

    &__category {
        font-size: 0.8125rem;
        letter-spacing: 0.3125rem;
        text-transform: uppercase;
    }

    &__title {
        font-size: 2rem;
        font-family: var(--ff-fraunces);
        color: var(--veryDarkBlue-nut-900);
    }

    &__current-price {
        font-size: 2rem;
        font-family: var(--ff-fraunces);
        color: var(--clr-darkCyan-prm-400);
    }

    &__btn {
        cursor: pointer;
        text-decoration: none;
        display: inline-flex;
        gap: 0.5rem;
        justify-content: center;
        align-items: center;
        border: 0;
        border-radius: 0.5rem;
        padding: 0.75em 1.5em;
        background-color: var(--clr-darkCyan-prm-400);
        color: var(--white-nut-100);
        font-weight: var(--fw-bold);
        font-size: 0.925rem;

        &:is(:hover, :focus) {
            background-color: var(--clr-darkCyan-prm-hover);
        }

        &[data-icon="cart-icon"]::before {
            content: "";
            background-image: url("../images/icon-cart.svg");
            width: 15px;
            height: 16px;
        }
    }
}
```

## Author

- Github - [hassanidris](https://github.com/hassanidris)
- Frontend Mentor - [@hassanidris](https://www.frontendmentor.io/profile/hassanidris)
