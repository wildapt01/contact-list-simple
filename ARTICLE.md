# Creating a contact list with vanilla JS, HTML and CSS

This is a simple project which is part of a series of articles I'd like to present. As it's the first one, we are starting, well, simple. Vanilla JS, HTML and CSS. The plan is to create the same type of app first like it is presented here then do a second iteration with some frameworks and libraries like Node.js, React.js, Postgres and a few more doodas.

### Preliminary about the tooling

Like for a lot of developers, Visual Studio Code is my main coding tool. I tried other editors and VSC has still my vote. The numerous extensions are a blessing and I use them a lot! You're totally free to feel otherwise, this is completely fine. But VSC is still great. I mean it. Just sayin'...

My environment is Windows 10 (all right, keep the flaming to the minimum) because I work in an organisation which is a total Microsoft shop. I also confess I like Windows (Gasp!). My terminal runs in Ubuntu 20.04 through WSL2 directly in VSC. My redeeming quality is that I really like Linux too. There may be still some hope that I avoid eternal damnation. My repos live on GitHub where the complete app can be found HERE. Don't hesitate to add a star on GitHub and/or a clap on Medium if you like, as well as a comment.

For the present app, we are using vanilla Javascript (ES6), HTML5 and CSS3. Nothing else. So let's start.

### Initial set-up

Let's create the repo first, I called it `contact-list-simple`, a very original repo name... Clone it to your machine and launch it with your favorite editor. Let's fire a terminal in VSC or in a separate window and create the skeleton for our app by typing:

```
mkdir scripts styling assets
touch index.html scripts/index.js scripts/data.js scripts/input-validation.js styling/style.css
```

In 2 lines, the necessary 3 folders and 5 files are created. The folder `assets` will host an image file for the background. The folder `scripts` will have all the source code obviously, and `styling` the CSS files. Nothing new here, just plain and simple organisation.

Copy your favorite image in PNG format into the `assets` folder. I added a favicon just because its absence will pop an error in the browser (Chrome) and my OCD side doesn't like errors... Open `index.html` to start the page and linking stuff. By typing a bang `!` in VSC we have the basic HTML skeleton for our page, like so:

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Document</title>
  </head>
  <body></body>
</html>
```

In the `<title>` tag, we replace "Document" with our title: "My Contact List". In the `<body>` tag, we'll add `<h2>This is working!</h2>` to check that our page correctly displays in the browser. Finally, we link the code and style files as well as the files in `assets` and the Source Sans Pro font from Google Fonts, our `index.html` file should look like this:

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />

    <!-- Favicon -->
    <link sizes="32x32" href="/assets/" rel="icon" type="image/png" />
    <!-- Source Sans Pro font from Google fonts -->
    <link rel="preconnect" href="https://fonts.gstatic.com" />
    <link
      href="https://fonts.googleapis.com/css2?family=Source+Sans+Pro:wght@400;600&display=swap"
      rel="stylesheet"
    />
    <!-- Local style sheet -->
    <link href="styling/style.css" rel="stylesheet" />
    <!-- Scripts -->
    <script src="scripts/index.js" type="module" defer></script>

    <title>My Contact List</title>
  </head>
  <body>
    <h2>This is working!</h2>
  </body>
</html>
```

We are now in need of some data to create the contact cards. As this is the simplest version, we're going to work with static dummy data. Feel free to use your prefered way or even type a dozen contacts in an array in `data.js`. Being the lazy dude I am, I created the list in [Mockaroo](https://mockaroo.com/) and copied the resulting dummy data in `data.js`.
