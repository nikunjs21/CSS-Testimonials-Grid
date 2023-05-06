# Frontend Mentor - Testimonials grid section solution

This is a solution to the [Testimonials grid section challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/testimonials-grid-section-Nnw6J7Un7). Frontend Mentor challenges help you improve your coding skills by building realistic projects. 

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

- View the optimal layout for the site depending on their device's screen size

### Screenshot

![](./screenshot.jpg)

Add a screenshot of your solution. The easiest way to do this is to use Firefox to view your project, right-click the page and select "Take a Screenshot". You can choose either a full-height screenshot or a cropped one based on how long the page is. If it's very long, it might be best to crop it.

Alternatively, you can use a tool like [FireShot](https://getfireshot.com/) to take the screenshot. FireShot has a free option, so you don't need to purchase it. 

Then crop/optimize/edit your image however you like, add it to your project, and update the file path in the image above.

**Note: Delete this note and the paragraphs above when you add your screenshot. If you prefer not to add a screenshot, feel free to remove this entire section.**

### Links

- Solution URL: [Add solution URL here](https://your-solution-url.com)
- Live Site URL: [Add live site URL here](https://your-live-site-url.com)

## My process

### Built with

- CSS Grid

### What I learned

CSS Grid

To see how you can add code snippets, see below:

```html
<div class="container">
    <div class="card">
      <div class="personal-info">
        <div class="danial avatar"></div>
        <div class="info-text">
          <h4>Daniel Clifford</h4>
          <p>Verified Graduate</p>
        </div>
      </div>
      <h3 class="subject">
        I received a job offer mid-course, and the subjects I learned were current, if not more so, 
        in the company I joined. I honestly feel I got every penny’s worth.
      </h3>
      <h4 class="quote">
        “ I was an EMT for many years before I joined the bootcamp. I’ve been looking to make a 
        transition and have heard some people who had an amazing experience here. I signed up 
        for the free intro course and found it incredibly fun! I enrolled shortly thereafter. 
        The next 12 weeks was the best - and most grueling - time of my life. Since completing 
        the course, I’ve successfully switched careers, working as a Software Engineer at a VR startup. ”      
      </h4>
    </div>
    <div class="card">
      <div class="personal-info">
        <div class="jonathan avatar"></div>
        <div class="info-text">
          <h4>Jonathan Walters</h4>
          <p>Verified Graduate</p>
        </div>
      </div>
      <h3 class="subject">
        The team was very supportive and kept me motivated
      </h3>
      <h4 class="quote">
        “ I started as a total newbie with virtually no coding skills. I now work as a mobile engineer 
  for a big company. This was one of the best investments I’ve made in myself. ”    
      </h4>
    </div>
    <div class="card">
      <div class="personal-info">
        <div class="jeanette avatar"></div>
        <div class="info-text black">
          <h4>Jeanette Harmon</h4>
          <p>Verified Graduate</p>
        </div>
      </div>
      <h3 class="subject black">
        An overall wonderful and rewarding experience
      </h3>
      <h4 class="quote black">
        “ Thank you for the wonderful experience! I now have a job I really enjoy, and make a good living 
  while doing something I love. ”
      </h4>
    </div>
    <div class="card">
      <div class="personal-info">
        <div class="patrik avatar"></div>
        <div class="info-text">
          <h4>Patrick Abrams</h4>
          <p>Verified Graduate</p>
        </div>
      </div>
      <h3 class="subject">
        Awesome teaching support from TAs who did the bootcamp themselves. Getting guidance from them and 
  learning from their experiences was easy.
      </h3>
      <h4 class="quote">
        “ The staff seem genuinely concerned about my progress which I find really refreshing. The program 
  gave me the confidence necessary to be able to go out in the world and present myself as a capable 
  junior developer. The standard is above the rest. You will get the personal attention you need from 
  an incredible community of smart and amazing people. ”
      </h4>
    </div>
    <div class="card">
      <div class="personal-info">
        <div class="kira avatar"></div>
        <div class="info-text black">
          <h4>Kira Whittle</h4>
          <p>Verified Graduate</p>
        </div>
      </div>
      <h3 class="subject black">
        Such a life-changing experience. Highly recommended!
      </h3>
      <h4 class="quote black">
        “ Before joining the bootcamp, I’ve never written a line of code. I needed some structure from 
  professionals who can help me learn programming step by step. I was encouraged to enroll by a former 
  student of theirs who can only say wonderful things about the program. The entire curriculum and staff 
  did not disappoint. They were very hands-on and I never had to wait long for assistance. The agile team 
  project, in particular, was outstanding. It took my learning to the next level in a way that no tutorial 
  could ever have. In fact, I’ve often referred to it during interviews as an example of my developent 
  experience. It certainly helped me land a job as a full-stack developer after receiving multiple offers. 
  100% recommend! ”
      </h4>
    </div>
  </div> 
```
```css
:root {
    --moderate-violet: hsl(263, 55%, 52%);
    --very-dark-grayish-blue: hsl(217, 19%, 35%);
    --very-dark-blackish-blue: hsl(219, 29%, 14%);
    --white: hsl(0, 0%, 100%);
    --light-gray: hsl(0, 0%, 81%);
    --light-grayish-blue: hsl(210, 46%, 95%);
}

*{
    box-sizing: border-box;
    font-family: 'Comfortaa', cursive;
    font-stretch: normal;
}

body{
    font-size: 13px;
}

.container{
    width: 100%;
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    gap: 1.6rem;
    padding: 10px;
}

.card{
    border-radius: 10px;
    /* border: 1px solid blue; */
    min-height: 200px;
    box-shadow: 2px 2px 8px 2px rgba(0, 0, 0, 0.3);
    padding: 25px;
}

.card:nth-of-type(1){
    grid-column: 1/3;
    background-color: var(--moderate-violet);
}

.card:nth-of-type(2){    
    background-color: var(--very-dark-grayish-blue);
}

.card:nth-of-type(3){
    grid-column: 1/2;
    grid-row: 2/3;
}

.card:nth-of-type(4){
    grid-column: 2/4;
    background-color: var(--very-dark-blackish-blue);
}

.card:nth-of-type(5){
    grid-column: 4/5;
    grid-row: 1/3;
}

@media (max-width: 375px) {
    .container { 
        grid-template-columns: 1fr; 
    }

    .card:nth-of-type(1){
        grid-column: 1/2;
        grid-row: 1/2;
        background-color: var(--moderate-violet);
    }
    
    .card:nth-of-type(2){
        grid-column: 1/2;
        grid-row: 2/3;
        background-color: var(--very-dark-grayish-blue);
    }
    
    .card:nth-of-type(3){
        grid-column: 1/2;
        grid-row: 3/4;
    }
    
    .card:nth-of-type(4){
        grid-column: 1/2;
        grid-row: 4/5;
        background-color: var(--very-dark-blackish-blue);
    }
    
    .card:nth-of-type(5){
        grid-column: 1/2;
        grid-row: 5/6;
    }
}

.personal-info{
    display: flex;
    align-items: center;
}

.info-text{
    color: var(--white);
    padding-left: 10px;
}

.info-text h4{
    margin: 0;
    margin-bottom: 4px;
}

.info-text p{
    opacity: 0.5;
    margin: 0;
    font-size: 10px;
}

.quote{
    opacity: 0.5;
}

.subject, .quote{
    color: var(--white);
}

.black{
    color: var(--very-dark-grayish-blue);
}

.avatar{
    height: 33px;
    width: 33px;
    background-size: cover;
    border-radius: 50%;
}

.danial{
    background-image: url('images/image-daniel.jpg');
    border: 1px solid rgb(170, 129, 235);
}

.jonathan{
    background-image: url('images/image-jonathan.jpg');
    border: 1px solid rgb(255, 255, 255);
}

.jeanette{
    background-image: url('images/image-jeanette.jpg');
    border: 1px solid rgb(255, 255, 255);
}

.kira{
    background-image: url('images/image-kira.jpg');
    border: 1px solid rgb(255, 255, 255);
}

.patrik{
    background-image: url('images/image-patrick.jpg');
    border: 1px solid var(--moderate-violet)
}
```
```js

```

## Author

- Frontend Mentor - [@yourusername](https://www.frontendmentor.io/profile/nikunjs21)
