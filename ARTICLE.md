# Creating a contact list with vanilla JS, HTML and CSS

This is a simple project which is part of a series of articles I'd like to present. As it's the first one, we are starting, well, simple. Vanilla JS, HTML and CSS. The plan is to create the same type of app first like it is presented here then do a second iteration with some frameworks and libraries like Node.js, React.js, Postgres and a few more doodas.

### Preliminary about the tooling

Like for a lot of developers, Visual Studio Code is my main coding tool. I tried other editors and VSC has still my vote. The numerous extensions are a blessing and I use them a lot! You're totally free to feel otherwise, this is completely fine. But VSC is still great. I mean it. Just sayin'...

My environment is Windows 10 (all right, keep the flaming to the minimum) because I work in an organisation which is a total Microsoft shop. I also confess I like Windows (Gasp!). My terminal runs in Ubuntu 20.04 through WSL2 directly in VSC. My redeeming quality is that I really like Linux too. There may be still some hope that I avoid eternal damnation. My repos live on GitHub where the complete app can be found HERE. Don't hesitate to add a star on GitHub and/or a clap on Medium if you like, as well as a comment.

For the present app, we are using vanilla Javascript (ES6), HTML5 and CSS3. Nothing else. So let's start.

### Initial set-up

Let's create the repo first, I called it `contact-list-simple`, a very original repo name... Clone it to your machine and launch it with your favorite editor. Let's fire a terminal in VSC or in a separate window and create the skeleton for our app by typing:

```
user@PCrig: .../contact-list-simple$ mkdir scripts styling assets
user@PCrig: .../contact-list-simple$ touch index.html scripts/index.js scripts/data.js styling/style.css
```

In 2 lines, the necessary 3 folders and 4 files are created.

The folder `assets` will host a `favicon` file and an image file for the background. I prefer having a favicon just to avoid that pesky 404 error in the browser when Chrome does not find it. The folder `scripts` will have all the source code obviously, and `styling` the CSS files. Nothing new here, just plain and simple organisation.

Copy your favorite favicon and image in PNG format into the `assets` folder. Open `index.html` to start the page and linking stuff.

```html

```
