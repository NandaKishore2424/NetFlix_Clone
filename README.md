# NetFlix_Clone
## Date: 10/07/2025
## Objective:
To create a modern, responsive navigation bar using CSS Flexbox, mimicking real-world websites like Netflix. This helps reinforce alignment, spacing, and layout structuring using Flexbox properties.

## Tasks:

#### 1. Structure the HTML Layout:
Use a ```<nav>``` tag as the main container.

Add a brand logo/title on the left using a ```<div> or <h1>```.

Add navigation links like Home, Menu, About, Contact, and Login using a ```<ul> with <li> and <a>```.

#### 2. Apply Flexbox for Layout:
Use display: flex on the ```<nav>``` container.

Use justify-content: space-between to align the logo and menu.

Use align-items: center to vertically center both sections.

Style list items with horizontal spacing using gap or margin.

#### 3. Style Like a Real-World Navbar:
Add background color (e.g., dark or gradient like Netflix/Zomato).

Style text with bold fonts, hover effects, and link styling.

Remove default ul and li styles (list-style: none, text-decoration: none).

#### 4. Bonus Enhancements:
Add a hover underline or button effect on links.

Make it responsive using flex-wrap or media queries.

Fix the nav bar to top with position: sticky.
## HTML Code:
```
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>NETFLIX</title>
    <link rel="stylesheet" href="style.css" />
  </head>
  <body>
    <section class="herosection">
      <div class="navigation-bar">
        <img src="netflix.png" alt="logo" id="logo" />
        <nav>
          <ul>
            <li><a href="">Home</a></li>
            <li><a href="">TV Shows</a></li>
            <li><a href="">Movies</a></li>
            <li><a href="">Recently Added</a></li>
            <li><a href="">My List</a></li>
          </ul>
        </nav>
        <div class="user-profile">
          <img src="search.png" alt="search" class="icons" />
          <img src="bell.png" alt="bell" class="icons" />
          <img src="user.png" alt="user" class="icons" />
        </div>
      </div>

      <div class="body-content">
        <div class="rating">
            <ul class="rating-ul">
                <li>7.5</li>
                <li>2018</li>
                <li>2 Seasons</li>
            </ul>
        </div>
        <h3>LOST IN SPACE</h3>
        <p>
          After crash-landing on alien planet, the Robinson family fight against
          all odds to survive and escape, but they're surrounded by hidden
          dangers.
        </p>
        <div class="body-btn">
          <button id="watch-btn" type="submit">WATCH</button>
          <button id="add-btn" type="submit">ADD TO LIST</button>
        </div>
      </div>
    </section>

    <section class="container2">
        <div class="categories">
            <ul>
                <li>Trending Now</li>
                <li>Popular</li>
                <li>Netflix Original</li>
                <li>Premiers</li>
                <li>Recently Added</li>
            </ul>
        </div>
        <div class="sub-categories">
            <ul class="sub-categories-ul">
                <li class="odd">Action</li>
                <li class="even">Adventures</li>
                <li class="odd">Anim</li>
                <li class="even">Biography</li>
                <li class="odd">Crime</li>
                <li class="even">Comedy</li>
                <li class="odd">Documentary</li>
                <li class="even">Drama</li>
            </ul>
        </div>

        <div class="movies">
            <div class="movie">
                <img src="money.png" alt="">
            </div>
            <div class="movie">
                <img src="interstellar.png" alt="">
                <h3></h3>
            </div>
            <div class="movie">
                <img src="fast.png" alt="">
                <h3></h3>
            </div>
            <div class="movie">
                <img src="f1.png" alt="">
                <h3></h3>
            </div>
            <div class="movie">
                <img src="karate.png" alt="">
                <h3></h3>
            </div>
            <div class="movie">
                <img src="kungfu.png" alt="">
                <h3></h3>
            </div>
        </div>
    </section>
  </body>
</html>
```
## CSS Code:
```
body{
    margin: 0;
    font-family:'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
}

.herosection{
    background-image: url('background.jpg');
    height: 600px;
    width: 100%;
    background-size:cover;
}

.navigation-bar{
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 10px;
    margin-top: 0;
    position: sticky;
    top: 0;
    left: 0;
    z-index: 10;
    background-color: rgba(41, 40, 40, 0.3); 
    backdrop-filter: blur(10px);       
    -webkit-backdrop-filter: blur(10px); 
}

#logo{
    width: 100px;
    height: 50px;
}

.icons{
    width: 20px;
    height: 20px;
}
nav{
    width: 40%;
}

li{
    color: white;
    list-style: none;
}

ul{
    display: flex;
    flex-direction: row;
    justify-content: space-around;
    padding: 0;
}

a{
    text-decoration: none;
    color: white;
    border-bottom: 3px solid transparent;
    transition: border-color 0.3s ease;
}

a:hover{
    border-bottom: 3px solid red;
    transition-duration: 0.3s;
}

.user-profile{
    display: flex;
    justify-content: space-between;
    width: 150px;
}

.body-content{
    padding-left: 100px;
    margin-top: 100px;
}

.rating-ul{
    width: 15%;
    display: flex;
    justify-content: space-between;
}

.rating-ul li{
    border-right: 2px solid red;
    padding-right: 20px;
    text-align: center;

}

.body-content h3, p{
    color: white;
}

.body-content h3{
    font-size:70px;
    padding: 0;
    margin: 0;
}

.body-content p{
    width: 500px;
}

#watch-btn{
    padding: 10px;
    width: 9%;
    background-color: red;
    border: none;
    color: white;
    border-radius: 20px;
    margin-right: 20px;
}

#watch-btn:hover, #add-btn:hover{
    cursor: pointer;
}

#add-btn{
    padding: 10px;
    width: 9%;
    background-color: rgb(67, 65, 65);
    border: none;
    color: white;
    border-radius: 20px;
}

.body-btn{
    margin-top: 30px;
}

.categories{
    background-color: rgb(55, 55, 55);
    margin: 0;
    padding: 10px;
}

.categories ul li{
    text-decoration: none;
    color: white;
    border-bottom: 3px solid transparent;
    transition: border-color 0.3s ease;
}

.categories ul li:hover{
    border-bottom: 3px solid red;
    transition-duration: 0.3s;
    cursor: pointer;
}

.sub-categories{
    background-color: rgb(41, 40, 40);
    padding: 10px;
    display: flex;
    justify-content:center;
}

.sub-categories-ul{
    width: 80%;
    display: flex;
    justify-content: space-between;
}

.odd{
    background-color: red;
    color: white;
    padding: 5px 20px 5px 20px;
    border-radius: 20px;
}

.even{
    background-color: rgb(32, 32, 32);
    color: white;
    padding: 5px 20px 5px 20px;
    border-radius: 20px;
}

.movies .movie img{
    width: 180px;
    height: 300px;

}

.movies{
    background-color: black;
    display: flex;
    justify-content: space-around;
}

.movie{
    margin-top: 10px;
}
```
## Output:
![image](https://github.com/user-attachments/assets/740311dd-ba1f-4dee-a739-8337f700a489)


## Result:
A modern, responsive navigation bar using CSS Flexbox, mimicking real-world websites like Netflix. This helps reinforce alignment, spacing, and layout structuring using Flexbox properties is created successfully.
