# 1-intro-to-html

### 🚀Challenge
Use the old <marquee> tag to make the h1 title scroll horizontally.

<marquee> <h1>My Terrarium</h1> </marquee>

## Assignment
Imagine you are designing, or redesigning, your personal web site. Create a graphical mockup of your site, and then write down the HTML markup you would use to build out the various elements of the site. You can use software of your choice, just make sure to hand-code the HTML markup. (Just a simple design is enough)
```html
<!DOCTYPE html>
<html>
<head>
    <title>My Website</title>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, sans-serif;
            line-height: 1.6;
            color: #212529;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }

        .site-header {
            background-color: #f8f9fa;
            padding: 1rem 0;
            box-shadow: 0 2px 4px rgba(0,0,0,0.1);
        }

        .site-header nav {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo a {
            font-size: 1.5rem;
            text-decoration: none;
            color: #212529;
            font-weight: bold;
        }

        .nav-links {
            display: flex;
            list-style: none;
            gap: 2rem;
        }

        .nav-links a {
            text-decoration: none;
            color: #495057;
            transition: color 0.3s ease;
        }

        .nav-links a:hover {
            color: #212529;
        }

        .hero {
            padding: 4rem 0;
            background-color: #f8f9fa;
            text-align: center;
        }

        .hero h1 {
            font-size: 2.5rem;
            margin-bottom: 1rem;
        }

        .lead {
            font-size: 1.25rem;
            color: #6c757d;
            margin-bottom: 2rem;
            max-width: 600px;
            margin-left: auto;
            margin-right: auto;
        }
        .featured-work {
            padding: 4rem 0;
        }

        .featured-work h2 {
            text-align: center;
            margin-bottom: 3rem;
        }

        .project-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
        }

        .project-card {
            background-color: #f8f9fa;
            border-radius: 4px;
            overflow: hidden;
            transition: transform 0.3s ease;
        }

        .project-card:hover {
            transform: translateY(-5px);
        }

        .project-image img {
            width: 100%;
            height: 200px;
            object-fit: cover;
        }

        .project-content {
            padding: 1.5rem;
        }

        .project-content h3 {
            margin-bottom: 0.5rem;
        }
        .site-footer {
            background-color: #f8f9fa;
            padding: 1rem 0;
            text-align: center;
            color: #6c757d;
        }
        
        @media (max-width: 768px) {
            .menu-toggle {
                display: block;
            }

            .menu-toggle span {
                display: block;
                width: 25px;
                height: 2px;
                background-color: #212529;
                margin: 5px 0;
            }

            .nav-links {
                display: none;
                position: absolute;
                top: 100%;
                left: 0;
                right: 0;
                background-color: #f8f9fa;
                padding: 1rem;
                flex-direction: column;
                align-items: center;
                gap: 1rem;
            }

            .nav-links.active {
                display: flex;
            }
        }
    </style>
</head>
<body>
    <header class="site-header">
        <nav class="container">
            <div class="logo">
                <a href="/">Blog Markup</a>
            </div>
            <ul class="nav-links">
                <li><a href="#work">Work</a></li>
                <li><a href="#about">About</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>
        </nav>
    </header>

    <main>
        <section class="hero">
            <div class="container">
                <h1>Welcome to my personal website!</h1>
                <p class="lead">I'm a CS student, a tech enthusiast and an aspiring artist. Check out my website to know more about me.</p>
            </div>
        </section>

        <section id="work" class="featured-work">
            <div class="container">
                <h2>My Interests</h2>
                <div class="project-grid">
                    <article class="project-card">
                        <div class="project-content">
                            <h3>Tech culture</h3>
                            <p>As a student majoring in AI, the new updates in the tech world draws me in, urging me to uncover more layers.</p>
                        </div>
                    </article>

                    <article class="project-card">
                        <div class="project-content">
                            <h3>Food & Travel</h3>
                            <p>Exploring new cultures and cuisines. Follow my socials to view more about my exciting adventures.</p>
                        </div>
                    </article>

                    <article class="project-card">
                        <div class="project-content">
                            <h3>Art</h3>
                            <p>What is life without a passion for art! Music has played an irreplacable role in my life. If you enjoy listening to music, do check out my song covers on Soundcloud.</p>
                        </div>
                    </article>
                </div>
            </div>
        </section>
    </main>

    <footer class="site-footer">
        <div class="container">
            <p>&copy; 2025 • Created by Malavika</p>
        </div>
    </footer>
</body>
</html>
```

# 2-intro-to-css

### 🚀Challenge
Add a 'bubble' shine to the left bottom area of the jar to make it look more glasslike. You will be styling the `.jar-glossy-long` and `.jar-glossy-short` to look like a reflected shine.

```css
.jar-glossy-long {
	width: 3%;
	height: 20%;
	border-radius: 2rem;
	background: #45dbe3;
	position: absolute;
	bottom: 20%;
	left: 5%;
}

.jar-glossy-short {
	width: 3%;
	height: 5%;
	border-radius: 2rem;
	background: #45dbe3;
	position: absolute;
	bottom: 45%;
	left: 5%;
}
```

## Assignment

Restyle the terrarium using either Flexbox or CSS Grid, and take screenshots to show that you have tested it on several browsers.

`index.html`
```html
<div id="page">
    <div class="flex-container">
        <div>
            <img class="plant" alt="plant" id="plant1" src="./images/plant1.png" />
        </div>
        <div>
            <img class="plant" alt="plant" id="plant2" src="./images/plant2.png" />
        </div>
        <div>
            <img class="plant" alt="plant" id="plant3" src="./images/plant3.png" />
        </div>
        <div>
            <img class="plant" alt="plant" id="plant4" src="./images/plant4.png" />
        </div>
        <div>
            <img class="plant" alt="plant" id="plant5" src="./images/plant5.png" />
        </div>
        <div>
            <img class="plant" alt="plant" id="plant6" src="./images/plant6.png" />
        </div>
        <div>
            <img class="plant" alt="plant" id="plant7" src="./images/plant7.png" />
        </div>
        <div>
            <img class="plant" alt="plant" id="plant8" src="./images/plant8.png" />
        </div>
        <div>
            <img class="plant" alt="plant" id="plant9" src="./images/plant9.png" />
        </div>
        <div>
            <img class="plant" alt="plant" id="plant10" src="./images/plant10.png" />
        </div>
        <div>
            <img class="plant" alt="plant" id="plant11" src="./images/plant11.png" />
        </div>
        <div>
            <img class="plant" alt="plant" id="plant12" src="./images/plant12.png" />
        </div>
        <div>
            <img class="plant" alt="plant" id="plant13" src="./images/plant13.png" />
        </div>
        <div>
            <img class="plant" alt="plant" id="plant14" src="./images/plant14.png" />
        </div>
    </div>
```
`style.css`
```css
.flex-container {
    display: flex;
    flex-direction: row;
    justify-content: center;
    background-color: #aac3e1;
    width: 100%;
    left: 0px;
    top: 0px;
    height: 100%;
    padding: 20px;
}
```

# 3-intro-to-DOM-and closures

## Assignment

`DocumentFragment` is widely used in modern web development to optimize DOM manipulations for better performance. While it's not explicitly advertised, many websites and web applications—especially those with dynamic and interactive interfaces—use `DocumentFragment` behind the scenes to efficiently manage and update the DOM.

`DocumentFragment` is a lightweight container for holding DOM nodes without being part of the live document tree. It improves performance because:

- Batch DOM Updates: Modifying or appending elements to a DocumentFragment doesn't trigger DOM reflows or repaints until the fragment is appended to the live DOM.
- Efficient Rendering: It's faster to build a collection of elements in a DocumentFragment and insert them all at once rather than adding elements one at a time.

An e-commerce website like Amazon Amazon likely uses `DocumentFragment` (or similar optimizations) to efficiently render large numbers of dynamic elements, such as product listings, reviews, or recommendations, without causing performance bottlenecks. nstead of appending each product directly to the DOM, all the elements are first appended to a DocumentFragment.
The DocumentFragment is then appended to the live DOM in one operation, which minimizes reflows and repaints.


