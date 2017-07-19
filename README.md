# Pop-Up-Penguin

Get the penguin pngs!
Before we start, we need to make sure we have all the image files this project requires. If you haven’t already, download the file at the top of this page called penguin_pngs.zip.

Once you’ve downloaded the **zip** file make sure it’s in a place you can find it and open it to get at the files inside. It should be full of image files with the "png" extension.

## Step 1: Upload our penguins
Alright. Let’s start making our cute penguin game. The first thing we need to do is upload all our penguin images.

- Create the files: index.html, styles.css, and app.js
- Open or unzip the penguin_pngs.zip file in the location. You need the image files inside, not the zip itself.

## Step 2: Make some divs
![Step 2](https://raw.githubusercontent.com/junior-devleague/Pop-Up-Penguin/master/images/step_02.jpg)

Now that we’ve added all our files let’s start building our game. We’ll be adding a set of divs to our HTML and matching styles in our CSS that create the image above.

- Add the following code between the <body> tags of the HTML:

```html
<body>
    <div id="gameholder">
        <div id="title"></div>
        <div class="penguin1"></div>
        <div class="penguin2"></div>
        <div class="penguin3"></div>
        <div class="penguin4"></div>
        <div class="penguin5"></div>
        <div class="penguin6"></div>
        <div class="penguin7"></div>
        <div class="penguin8"></div>
        <div class="yeti"></div>
    </div>
</body>
```

*What this code is doing:*

These divs are defining the structure for our game. Notice the spacing and how we've set up a main container div called "game holder". Each “penguin” div will be a little bump of snow hiding a penguin (or yeti). We will be adding the images to them in the CSS.

Next, go to the styles.css file.

*Add the following code to the CSS tab:* 

```html
//write all your code beneath the comments.
body {
    //add a background color of #ccf5f5
  
}
#gameholder {
    //set the width of 600px

    //set the margin left to auto

    //set the margin right to auto

}
#title {
    //set the width to 600px

    //set the height to 150px
    
    //set the background image to an empty url

}
```

*What this code is doing:*

body is making our background a nice blue color.

"gameholder" is making our gameholder div 600px wide and centering it in the screen. It’s invisible, but helps us organize our other elements.

title is setting a size for our our title div and giving that div a background image. In this case that image happens to be the title/instructions to our game. We’ll add that in the next step.

- Now look in the project tab.
- Find the file called: **penguin_title.png**
- Put your cursor between the (' and ') at the end of the background image property, right between the quotes, and click “paste to code” in the media panel. This copies the image url to your code at the location of your cursor.
Save and take a look at the preview window. You should see some snow covered lettering that says “Find the Penguins.”

We’ve got our title, let’s add some little snow-covered mounds for our penguins!

*Add the following class to the CSS tab:*

```html
.penguin1 {
    //set the width to 200px

    //set the height to 200px
    
    //set the float to left

    //set the background image to an empty url

}
```

- Now look in the project tab.
- Find the file called: **mound_1.png**
- Put your cursor between the (' ') at the end of the background image property and click “paste to code”

*All of our CSS looks like this so far:*

```html
body {
    background-color: #ccf5f5;
}
#gameholder {
    width: 600px;
    margin-left: auto;
    margin-right: auto;
}
#title {
    width: 600px;
    height: 150px;
    background-image:url('/penguin_pngs/penguin_title.png');
}
.penguin1 {
    width: 200px;
    height: 200px;
    float: left;
    background-image:url('/penguin_pngs/mound_1.png');
}
```

### To finish this step:

Copy the .penguin1 class and use it to make styles for .penguin2 through .penguin8. Make a .yeti class as well. You’ll find image files for each one labeled in the Media folder.

## Step 3: Add a rollover
![Step 3](https://raw.githubusercontent.com/junior-devleague/Pop-Up-Penguin/master/images/step_03.jpg)

Now let’s add a rollover or :hover effect to each one of our mounds. This will pop up a question mark and jiggle the snow a little adding intrigue and suspense to our game.

In the CSS tab find our .penguin1 class.
Make a new line above the class and add the following style:

```html
//create a hover pseudo selector to the penguin1 class
.penguin1:hover {
    //set the background image to an empty url

    //set the cursor to a pointer

}
```

This style is what’s called a pseudo-class. It’s a way to add effects and additional styles to elements that we’ve already created. In this case we will be changing the background image of that div when a mouse is over it. We will also be changing the cursor to a pointer, or little hand giving our users another clue that the mound is clickable.

Go into the Media tab and find the image for mound_1_hover.png.
Paste the image link inside the quotes ('') of the background-image property.
Go to the preview mode and run your mouse over the first mound. Did the question mark pop up? That’s :hover doing its job.
To finish this step:

Make new :hover classes for each of our .penguin and .yeti classes. You can find the images in our media folder.

## Step 4: Pop up the penguins!
![Step 4](https://raw.githubusercontent.com/junior-devleague/Pop-Up-Penguin/master/images/step_04.jpg)

Now that we’ve got our mounds tempting us with those question marks, let’s hide some penguins (and a yeti!) inside each one and use another pseudo-class to make them pop up when clicked.

In the CSS tab find the .penguin1:hover class.
Underneath, that class add the following class:

```html
.penguin1:active {
    background-image:url('');
}
```

:active is another type of pseudo-class. Similar :hover it adds/changes the style of .penguin1 when the div is clicked with the mouse.

The position in the code of pseudo-classes is important. An :active class should always come after or underneath :hover in the code for the effect to work properly.

- Go into the media tab and find a penguin image. You can start with penguin_1.png.
- Paste the code for the image inbetween the (‘’)
- Go back to the preview and click the first mound. Did the penguin pop up? Hold your mouse button down to keep the penguin from popping back down.
To finish this step:

Make new :active classes for each of our .penguin and .yeti classes. Add penguin images from the media tab. Make sure you hide the Yeti somewhere too.

## Step 5: Yeti alert!
![Step 5](https://raw.githubusercontent.com/junior-devleague/Pop-Up-Penguin/master/images/step_05.jpg)

We’ve got all our penguins and yeti in place. Let’s add a yeti alert that will pop up when the yeti is clicked!

In your html file:
```html
<div class="yeti" onmousedown="roar()"></div>
```

In your app.js file:
```html
function roar(){
    //create and alert function that passes in the string parameter "RAAAAAAWWWWRRRRR"
    
}
```

This is a little bit of Javascript that will pop up a browser alert with the text “Yaaaarrrr” when you press your mouse button on the yeti. Try it out in the preview mode. To learn more about Javascript try playing around with the Night and Day project next.

## Step 6: Mix it up and challenge someone
![Step 6](https://raw.githubusercontent.com/junior-devleague/Pop-Up-Penguin/master/images/step_06.jpg)

Now that we’ve got all our penguins (and yeti) hidden let’s play the game! Find a friend and challenge them to find all the penguins without accidently clicking on the yeti.

After they’ve had a go, mix the classes up in your HTML to reshuffle the mounds and let them try again. To make it extra challenging, change the images in the :active states to put different penguins (and your yeti) under different mounds.

## To finish this step:

Teach your playing partner how to change the images in the :active states and trade off challenging each other to a game of “Find the Penguins.”

## Stretch Goals
- Double or triple the number of mounds to make the game more challenging! You can use the same penguin png files more than once if you like but you’ll need to make more divs and classes. Be creative, try and add your own png files if you can! Also! Add some sounds each squeak, squawks, and roars!
- Replace the images with your own images.
- Create levels of the game with each level increasing the mounds.

Let your instructor know!

## Resource
- Review Pseudo Selectors: https://www.w3schools.com/css/css_pseudo_classes.asp
- Intro to JS Functions: https://www.w3schools.com/js/js_functions.asp
- Intro to JS Events: https://www.w3schools.com/js/js_events.asp

