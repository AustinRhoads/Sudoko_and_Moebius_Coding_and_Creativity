
![Image](./moebius_walls.jpg)
###                                                                        _Star Wars concept art_ -Moebius


When I think of creativity, immediatly the french painter Jean Giraud, "Moebius", pops into my head. His work is other-worldly and extremely imaginitive as is evident in his costume and set design of the movie _The Fifth Element_. Most people dont associate creativity with a technical skill such as coding. However, creativity and critical thinking have always gone hand in hand. Simply observe the works of any great artist to see the vast technical skill coupled with personal vision.

As a newb entering into the world of coding, I am pleased to find many opportunities to get creative. Problem solving is a great example of a springboard for creativity. The harder the problem the more deeply we can look into the critical nature of what we are trying to accomplish. This pushes us to learn new things and to innovate.

My first real portfolio project is a Ruby CLI app called find-a-park-cli. This app allows users to search by state and by activity to view a matching list of national parks. It's an exercise in object oriented programming. All data is parsed from the National Parks website by using the Nokogiri gem. Throughout the process of building this app I was able to learn new things and explore alternitive ways to solve problems. My first big problem came while working with the Nokogiri gem.

 
 
 
 

# Nokogiri and Sudoku


Nokogiri is a Ruby gem used to parse files such as HTML. It's name comes from the Japanese fine toothed saw (which, as a woodworker, I own one and they are awesome!). Thus far I could find what I was looking for by a simple two part process; First, inspect the page and find the element with the selector tool. Second, do a bit of fishing until you return the desired data. I thought this was going to be an easier part of the process, but this proved to be untrue.

The National Parks website I was to scrape had a form of selectable elements, such as, the state and the activity to filter the search results. Scraping the state and activity names went by quickly and soon after I pulled the URL associated with each search result. I searched Alaska and fishing. One of the results was Lake Clark. I knew If I could pull the text "Lake Clark" the rest of the data would come quickly. However this didn't happen. I played around with selecting the parent elements by ID, by class name and nothing worked. Eventually I printed all the XML nodes searching for the string "Lake CLark" but it was nowhere to be found. I love problem solving but I admit this was a _bit_ frustrating so I decided to take a break and take on a problem I knew I could solve, a sudoku puzzle.

What I love about sudoku is that all the answers you need are already there waiting to be discovered. I was thinking about this when I remembered something I had learned to do with javascript, class toggle.
Basically, class toggle works like this... say you have a list of _park_ objects. You give each _park_ the class name "unselected". Elements would only be displayed on the HTML if they have a "selected" class. What toggle does is switches the class name from "unselected" to "selected" or visa versa to display or not display a _park_ within the HTML. This meant that somewhere on that page was data on every single park. I inspected the site's sources and sure enough I found a Json file with every single park listed with all activities and states associated with the park! I didn't know a thing about Json but it didn't matter. I could parse everything I needed from the text of this file with one scrape. All the answers I needed were in one place waiting to be discovered.
Often creativity is the product of gaining a new perspective. Sometimes it's best to take a break and look at a problem with fresh eyes.






# Object Oriented Programming


At this point, my app had the data it needed but other than that it was as baren as a desert so I had to start building objects, _states_, _parks_ and _activities_.
Essentially, everything in Ruby is an object. From strings and integers to class instances and even class itself. An object is how we define talking about a thing. It is also a function, it defines how it interacts with other things. A state is not only a name and abbreviation, "California, CA", but also a state can have many parks, multiple states can have access to those parks, and there should never be more than one state with the same name. However, the state itself is not equal to it's name. A state is a state and any instance of a _state_ or a _park_ should reflect a real state or park as much as possible. I believe this to be an important distinction in OOP as it's concievable that a park could change it's name and in theory this should be the same instance of a _park_ object. Another example would be if two different parks went by the same basic name and had the same general location ( which is the case for Natchez Trace scenic trail and Natchez Trace parkway in Alabama). If an object was defined soley by it's name many parks would not be created in an attempt to control redundancy. What this tells me is that as much as I try to make the _state_ class like a real state it will always be an artifact designed by me and how I define things critically effects my own creative vision. So I must always keep this in mind as im writing code.
In my case I can use the url as the control factor. No two parks even with the same name should ever have the same URL.






#  Make it Better 

The find-a-park-cli app came about sort of organically. I built stuff when I needed it but now I needed it to work better. When the app is launched the user is prompted to select a state and then select an activity to search by. As each list is pulled up there was a bit of a lag while it was being scraped and since a user could search for parks multiple times I didn't want this to be experienced at each search. The solution was to scrape both lists only once and assign them to a variable before the app prompts the user. Then I could refer to these variables throughout the app preventing a rescrape. Tidying up the code like this made the user interface flow better. Adding a loading bar to when the parks are being scraped (via the Ruby-ProgressBar gem) makes the "dead-time" a user would experience more palatable. Finally, I did some playing around with colorize in both form and function, making all selectable items one color and selected items another. There is something statifying in seeing your idea getting polished up like this. (The same is true in woodworking.) 






# Final thoughts 


Creativity comes from solving problems and gaining new perspective. Hitting a wall is the best oppotunity to to let your imagination explore its inventiveness. Critical thinking is a tool we can use to make our vision come to fruition. Coding is so much fun! Get out there and make something yourself!!!

