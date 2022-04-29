# Frontend Mentor - QR code component solution

This is a solution to the [QR code component challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/qr-code-component-iux_sIO_H). Frontend Mentor challenges help you improve your coding skills by building realistic projects.

## Table of contents

  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
  - [Continued development](#continued-development)
  - [Useful resources](#useful-resources)
- [Author](#author)


**Note: Delete this note and update the table of contents based on what sections you keep.**


### Links

- Solution URL: [Add solution URL here](https://your-solution-url.com)
- Live Site URL: [Add live site URL here](https://your-live-site-url.com)

## My process

I started with laying out my HTML to build the structure for my page. I first added a div for the flexbox container followed by a div for the box container. Inside the box container I added additional divs for the contents of the box leaving the prewritten attributions div out side of both the flexbox and box containers.

After writing up my HTML I made an external styles.css sheet and linked it under the title in my head section. Next I reviewed the style-guide.md. I then pulled up the suggested font on google fonts and added the links for the font style and weights listed.

Once my links for fonts and external style sheet was added I started writing my css starting from my top div all the way to the bottom. I referenced mdn web doc's to help me put the pieces together along with some stackoverflow pages to help me get my alignment just right. Pages I found helpful will be listed below!

### Built with

- Semantic HTML5 markup
- CSS custom properties
- Flexbox

### What I learned

I learned a lot about what to do and what NOT to do when building your flexbox to act the way you want/need it to. I really had no idea how to use css flexbox before starting this and combed my way through mdn and stack overflow to finally put it together. When I first started I only had my flex-container div with the content div's placed inside. I styled .flex-contaner in the way my .box div is currently styled now, and couldn't figure out how to make the container stay centered on my page when my screen changed sizes. After finding a stackoverflow Q&A about the same issue I created the .box div inside my .flex-container to hold all my content div's and adjusted my css styling from there.

```HTML
original html
<div class="flex-container">

    <div class=qr-code>
      <img src="images/image-qr-code.png" alt="QR-Code" />
    </div>

    <div class="qr-text">
      <p class="p-1">
        Improve your front-end skills by building projects
      </p>
      <p class="p-2">
        Scan the QR code to visit Frontend Mentor and take your coding skills to the next level
      </p>
    </div>

  </div>
  ```
  ```HTML
  corrected html
  <div class="flex-container">
    <div class="box">

      <div class=qr-code>
        <img src="images/image-qr-code.png" alt="QR-Code" />
      </div>

      <div class="qr-text">
        <p class="p-1">
          Improve your front-end skills by building projects
        </p>
        <p class="p-2">
          Scan the QR code to visit Frontend Mentor and take your coding skills to the next level
        </p>
      </div>

    </div>
  </div>
  ```
  ```css
  original css (it was a mess!)
  .flex-container {
    display: flex;
    position: absolute;
    flex-direction: column;
    align-items: center;
    width: 320px;
    height: 479px;
    left: 800px;
    top: 152px;
    background-color: white;
    border-radius: 20px;
    box-shadow: 0px 25px 25px 0px rgba(0, 0, 0, 0.0476518);
    ```
    ```css
    corrected css
    .flex-container {
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      height: 100%;
      padding: 200px
    }

    .box {
      flex: 0 0 100%;
      width: 320px;
      height: 490px;
      background-color: white;
      border-radius: 20px;
      box-shadow: 0 45px 45px 0 rgba(0, 0, 0, 0.0476518);
    }
    ```

### Continued development

I really want to continue expanding on flexbox and really grasp the concepts. I think continuing projects like this and teaching myself through mdn and other sources found through googling the issues I come across will help me build those skillsets and memory. Finding and working through the issues on my own helps me so much more than following along with a teacher or video.

### Useful resources

- [Flexbox resource] (https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Flexible_Box_Layout/Basic_Concepts_of_Flexbox) - This really helped me with understanding what flexbox is and what it's used for, along with all the properties used.
- [Flexbox alignment](https://stackoverflow.com/questions/40776581/why-isnt-my-flex-item-aligning-in-the-center) - This REALLY helped my finally put my page together correctly it showed me what I was doing wrong with my original .flex-container set up. This page and especially the answer from Michael Benjamin and the helpful link he added for reference!
- [Flexbox stackoverflow reference](https://stackoverflow.com/questions/32551291/in-css-flexbox-why-are-there-no-justify-items-and-justify-self-properties) - This is the link added by Michael Benjamin in his helpful answer referenced above. This helped me SO MUCH! this had so much more information on it than I had found anywhere else!
- [css box-shadow](https://developer.mozilla.org/en-US/docs/Web/CSS/box-shadow) - This helped me learn about css box-shadow. This is something I hadn't used before this project. The also have an amazing box-shadow generator you can use to get the shadow exatly how you want it!
- [css box-shadow tool](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Backgrounds_and_Borders/Box-shadow_generator) - I loved using this generator! It really helped me understand exactly what each value does for the shadow you're creating!

## Author

- Website - [Elizabeth Marker](https://emarker314.github.io)
- Frontend Mentor - [@yourusername](https://www.frontendmentor.io/profile/yourusername)
