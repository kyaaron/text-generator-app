# Text Generator Application
This is a text generator application I made to help with work. In my Pega Developer position, I needed a lightweight tool to generate text to match character counts in order to test certain features of our team's application. The text generators on the internet were slow, partly due to some having feature bloat and others loading slower on a government computer. So I made a simple text generator that collected no data from the user.

**Link to project:** https://kyaaron.github.io/text-generator-app/

## How it's made
I used vanilla HTML5 and CSS3 on the front end and found a visually nice dark-mode color palette to use. In the script.js file, I have a short string of Lorem Ipsum text. The `generateChars()` function loops through the short string of text and adds each character (letter and space) to an array up until the character count number given by the user is reached. Then it breaks and joins the array into a string which is returned. There are event listeners attached to each button to add the text to the DOM, remove the text, and copy to the clipboard (using the Navigator API to copy the text to the Clipboard object).

## Optmization
- It would be great to clean up the code to use fewer global variables
- I could add the inverse operation of counting characters inputted by a user

## Lessons Learned
I learned about the Navigator API and Clipboard object, where you can instruct code to add values to the clipboard without manually having the user select + copy. I also learned about getting the value from an `<input>` element and using that value in other places in my code, which I have since implimented in other projects. Another neat thing I learned to help with the presentation was the use of `overflow-y: auto;` and `scrollbar-width: thin;` CSS rules, which add a scrollbar to the returned string section if the content overflowed that section. This was a suggestion from one of my coworkers, and it made for a much better UI/UX when, for example, a user needed to generate a string of text over 4000 characters.
