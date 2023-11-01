## Open Camp Week 1

In Week 1 (W1), we will cover the basics of HTML and CSS, which are essential
languages that you need to know in order to build websites.

At the end of this week, you should be able to understand the following:

- What HTML and CSS are
- Use HTML with templates build simple websites
- Use simple CSS to style different elements of the website

We will continue with HTML and CSS in Week 2 (W2) for you to design different
types of layouts.

You may wish to test out various HTML tags and see how they look like
on your web browser. You can use the following code to test out various tags:

```
<!DOCTYPE html>
<html lang="en">
    <head>
        <title>Hello!<title>
    </head>
    <body>
        <!-- Put the HTML tag you wish to test within the body tag -->
        <!-- This is a comment and will not show up on your browser. -->


    </body>
</html>
```


### Overview of W1

1. [CS50W Week 0][cs50w-0]: HTML and CSS
    - Watch until 1:25:00 which covers HTML and CSS
    - Go through the review questions as you complete the HTML and CSS sections

We will revisit the remaining parts of the video (Responsive Design and
Bootstrap) in future lessons.

2. Live Session #1: HTML Review
    - HTML practice and basics

3. Live Session #2: CSS Review
    - CSS practice and basics

4. [CS50x 2023: Lecture 0][cs50x-1] (2 hrs 9 mins)
    - Watch until 00:56:07 (Stop before they cover Algorithms)
    - Not required to complete this week's assignments (required for Week 2)
    - This lecture covers the basics of Computer Science, such as Binary numbers, algorithms
    - Review questions will be in Week 2


### Review Questions

**HTML**

1. Look at the following HTML code. Can you identify 2 errors with the following
code and explain why they are errors?

```
<!DOCTYPE html>
<html lang="en">
    <head>
        <title>Hello!<title>
    </head>
    <body>
        Hello, world!
    </html>
</body>
```

<details>
  <summary>Answers for Question 1</summary>

  1. The closing tag for `<title>` should have been `</title>`
  2. `<body>` should be closed first (`</body>`), followed by `<html>`
  (`</html>`). HTML Tags in the inner portion of another HTML tag should be
  closed first before the outer one.
  
</details>

---

2.  Are there any ***visual differences*** using the HTML code in
Review question 1 versus the corrected version of it with no errors?

(Try opening both versions of the code with and without errors on your web
browser. Do they look the same?)

<details>
  <summary>Answers for Question 2</summary>

  HTML is known to be super forgiving when our web browsers render them, and very rarely will they will show error messages for wrong HTML. In this case, since the errors are minor, there should be no visual differences at all.

  In future, as you work on more complicated designs, you may start noticing differences.
  
</details>

---

3. An `<img>` image tag can be used to display an image. Why does it not require
a closing tag, eg. `</img>`?

<details>
  <summary>Answers for Question 3</summary>

  An image is just a single HTML element that can't really have anything inside of it.
  It is one of the few HTML tags that do not need to have a closing tag (they
  are self-closing).
  
  Another common one is the `<input>` tag, which is used to create input fields
  inside forms.
  
</details>

---

4. Why does the `<img>` tag not require a closing tag?

<details>
  <summary>Answers for Question 4</summary>

  An image is just a single HTML element that can't really have anything inside of it.
  It is one of the few HTML tags that do not need to have a closing tag (they
  are self-closing).
  
  Another common one is the `<input>` tag, which we will cover in W2 
  when designing forms for users to input data.
  
</details>

---

5. Which of the following are not valid attributes for an `<img>` tag?

    ```
    1. `href`
    2. `src`
    3. `alt`
    4. `width`
    ```

<details>
  <summary>Answers for Question 5</summary>

  Only `1. href` is not a valid attribute for the `<img>` tag.

  For images, you use the `src` attribute (source attribute) to tell the browser
  where to find the image to be display.
  
  `alt` is used to tell screen readers (for users with accessibility needs) what
  the image is about (a short description).
  
  Finally, `height` and `width` are attributes that lets you define how tall and
  how wide the image should be in pixels respectively.

  Here's an example of an image tag to show a photo of a tree, with its
  corresponding `alt` tag and its width and height attributes defined.
  
  <img src="tree.jpg" alt="A photo of a single tree" width="800" height="400">

  As mentioned in the lecture videos, there are other ways to define the width
  and height of an image using CSS as well, which we will cover in W2.

  Reference: Learn more about the [`img`][img-tag] on MDN docs.
  
</details>

---

6. Complete the following sample code to create a form to collect the user's name and email address.
   Write down the code that should go into (i), (ii), and (iii)


```
<!DOCTYPE html>
<html lang="en">
    <head>
        <title>Hello!</title>
    </head>
    <body>

        <form>
            <input name="name" type="____(i)____" placeholder="Your name">
            <input name="email" type="____(ii)____" placeholder="Your email">

            <input type="submit">
        ____(iii)____

    </body>
</html>
```

<details>
  <summary>Answers for Question 6</summary>

  
  ```
  <!DOCTYPE html>
  <html lang="en">
    <head>
      <title>Hello!</title>
    </head>
    <body>

        <form>
            <input name="name" type="text" placeholder="Your name">
            <input name="email" type="email" placeholder="Your email">

            <input type="submit">
        </form>

        </body>
    </html>
  ```

  The correct answers are (i) `text`, (ii) `email`, and (iii) `</form>`.

  There are many types of input that we will be using in future. If you would like a sneak preview, have a look at the reference document for input on MDN.

  Reference: [`input`][input-tag] tag on MDN
  
</details>

---

7. Recreate the following using HTML:

```
Places to visit in UK

- London
    1. Leicester
    2. Borough Market
    3. Tower Bridge
- Manchester
    1. Piccadilly Gardens
    2. AO Arena
```

<details>
  <summary>Answers for Question 7</summary>

  ```
  <!DOCTYPE html>
  <html lang="en">
    <head>
      <title>Places to visit</title>
    </head>
    <body>
        <p>Places to visit in UK</p>

        <ul>
            <li>London
                <ol>
                    <li>Leicester</li>
                    <li>Borough Market</li>
                    <li>Tower Bridge</li>
                </ol>
            </li>
            <li>Machester
                <ol>
                    <li>Piccadilly Gardens</li>
                    <li>AO Arena</li>
                </ol>
            </li>
        </ul>

        </body>
    </html>
  ```

  You can easily nest more layers of unordered or ordered lists using the same
  way of nesting.
  
  Reference: [`ul`][ul-tag] and [`ol`][ol-tag] tags on MDN
  
</details>

---

**CSS**

8. Recreate the same HTML as question 7 (places to visit). Except this time, make sure that every list item has a unique colour using CSS.

<details>
  <summary>Answers for Question 8</summary>

  ```
  <!DOCTYPE html>
  <html lang="en">
    <head>
      <title>Places to visit</title>
    </head>
    <body>
        <p>Places to visit in UK</p>

        <ul>
            <li style="color: black;">London
                <ol>
                    <li style="color: blue;">Leicester</li>
                    <li style="color: red;">Borough Market</li>
                    <li style="color: green;">Tower Bridge</li>
                </ol>
            </li>
            <li style="color: gray;">Machester
                <ol>
                    <li style="color: pink;">Piccadilly Gardens</li>
                    <li style="color: purple;">AO Arena</li>
                </ol>
            </li>
        </ul>

        </body>
    </html>
  ```

  Here is an example of how you can specify different colors for each list item using CSS.

  `color` is used for the color of text.
  
  Reference: [`color`][css-color] on MDN
</details>

---

9. Design a `button` within a form that is 99 pixels wide and 129 pixels tall
using CSS. The button should say "I love CSS".

<details>
  <summary>Answers for Question 9</summary>

  ```
  <!DOCTYPE html>
  <html lang="en">
    <head>
      <title>Button</title>
    </head>
    <body>
        <form>
            <button style="width: 99px; height: 129px;">I love CSS</button>
        </form>
    </body>
  </html>
  ```

  In the lecture video, the instructor has demonstrated other ways to use CSS, such as writing CSS Styles within the `<head>` tag using the `<style>...</style>`.

  Try recreating this button with the `<style>` tag. 

**Assignments for W1**

- [A1: Creating a simple personal website pt. 1](../assignments/a1.md): Due by W1 Thursday 23:59
- [A2: Creating a simple personal website pt. 2](../assignments/a2.md): Due by W1 Sunday 23:59


[cs50w-0]: https://cs50.harvard.edu/web/2020/weeks/0/
[cs50x-1]: https://www.youtube.com/watch?v=IDDmrzzB14M
[img-tag]: https://developer.mozilla.org/en-US/docs/Web/HTML/Element/img
[input-tag]: https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input
[ol-tag]: https://developer.mozilla.org/en-US/docs/Web/HTML/Element/ol
[ul-tag]: https://developer.mozilla.org/en-US/docs/Web/HTML/Element/ul
[css-color]: https://developer.mozilla.org/en-US/docs/Web/CSS/color