# Creativity: 
## The red leaf maple forest in Guadalupe National Park, TX

When I think of creativity, typically someone like Brian Wilson, of the Beach Boys, or David Bowie pops into my head. Most people dont associate creativity with a tecchnical skill such as coding. Nor do they associate the colors of fall with the maple trees of west Texas. However, as I enter into the world of coding I am pleased to find many opportunities to get creative and I decided to make an app that connects people with the beauty of novel places such as the Guadalupe National Park.

Problem solving is a great springboard for creativity. The harder the problem the more deeply we can look into the critical nature of what we are trying to accomplish. This pushes us to learn new things and to innovate.

My first real portfolio project is a Ruby CLI app called find-a-park-cli. This app allows users to search by state and by activity to view a matching list of national parks. It's an excorcise in object oriented programming that utilizes the Nokogiri gem to scrape data off the national parks website. Throughout the process of building this app I was able to learn new things and explore alternitive ways of solving problems. My first big problem came very unexpectedly.

 

# Nokogiri: 
## Ice fishing in Lake Clark, Ak 
Nokogiri is a Ruby gem used to parse files such as HTML. It's name comes from the Japanese fine toothed saw (BTW I happen to own one and any woodworkers out there should try it if given the chance. Clean narrow cuts and some have both crosscut and ripsaw on either side of the blade! Super cool :) Anywho...) Thus far I could find what I was looking for by a simple two part process. First find the element with the selector tool and then do a bit of fishing until you return the desired data. This was, I thought, going to be the easiest part of the process. And it was, at first... then I caught a snag in the line. 
The National Parks website which I had to scrape had a form of selectable elements, such as, the state and activity to filter the search results. Scraping the state and activity names went by quickly and soon after I pulled the URL associated with each search result. I searched Alaska and fishing. One of the results was Lake Clark. I knew If I could pull the text "Lake Clark" the rest of the data would come quickly. However this didn't happen. I played around with selecting the parent elements by ID, by class name and nothing worked. I spent all day working on this without results. Eventually I printed all the XML nodes searching for the string "Lake CLark" but it was nowhere to be found. I love problem solving but I admit this was a _bit_ frustrating so I decided to take a break and take on a problem I knew I could solve, a sudoku puzzle. 
As I relaxed into solving this puzzle I thought, "What I love about sudoku is that all the answers you need are already there waiting to be descovered.", and then it all clicked!
From what I learned about javascript before I started school at Flatiron, you could toggle classes so that elements would only be displayed when given a "selected" class. This meant that somewhere on that page was data on every single park. I inspected the site's sources and sure enough I found a Json file with every single park listed with all activities and states associated with the park! I didn't know a thing about Json but it didn't matter. I could parse everything I needed from the text of this file. All the answers I needed in one place waiting to be discovered.


# Object Oriented Programming:
## Spring time in Death Valley, CA
Essentially, everything in Ruby is an object. An object is how we define talking about a thing. An object is also a function, it defines how it interacts with other things. A state is not only a name and abbreviation, "California, CA", but also in this context a state can have many parks, multiple states can have access to those parks, and there should never be more than one State with the same name. As much as I try to make the State class like a real state it will always be an artifact designed by me to serve my purpose and my purpose, in this instance, is to talk about the national parks.
My app was looking pretty bare.Some text here about how all the little critters come out in springtime. Objects are like creatures in an ecosystem that work in a mutually beneficial way. State object, Park objects, The Scraper and the cli class.


# conclusion: 
## Summer somewhere, SW
Creativity comes from solving big problems. Hitting a wall is the best oppotunity to to let your imagination explore its inventiveness.
## Welcome to GitHub Pages



### Markdown

Markdown is a lightweight and easy-to-use syntax for styling your writing. It includes conventions for

```markdown
Syntax highlighted code block

# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/AustinRhoads/Enter_the_Wild_Coding_and_Creativity/settings). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://help.github.com/categories/github-pages-basics/) or [contact support](https://github.com/contact) and we’ll help you sort it out.
