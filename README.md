# Data Visualization Project

## Data

The data I propose to visualize for my project is chess transfers from country to country between 2000 and 2017
[Dataset](https://gist.github.com/Patrick-Houlihan/601269a0a7811a08b1cd30f0e86aee1d)

## Prototypes

I do not yet have a prototype proof of concept as I'm focusing on prepping the dataset

1. Combining the country codes with country names for easier use (combining two datasets using java program)
2. Expanding dataset to include historical ranking, unknown how I'm going to tackle this one so far.

## Questions & Tasks

The following tasks and questions will drive the visualization and interaction decisions for this project:

 * What countries represent the highest average ratings of transferring players
 * How can I efficiently get this data from the FIDE ranking website (The tables retain the account ID's and date of transfer, FIDE retains historical ranking at the time)
 * Can I make a timelapse (or time slider) of this data showing where people go from year to year or month to month?
 * What countries show the highest brain drain, of talent leaving and not being replaced?
 * What are the highest rated players to transfer?

## Sketches

[sketch](https://drive.google.com/file/d/1PgeaZubEB8EJBcnl3BIacTizNZ1B2-zS/view?usp=sharing)

The idea for this sketch is a world map, HOPEFULLY a globe since 2D maps are weak (per this week's lecture) that you can click on a country and it will show you all the transfers to and from that region. Chess is a very nationalistic game at times, see the Cold War for examples of that, and some regions are significantly stronger than others. I'm curious to see how average transfered rating (skill level applies to chess). I want to see what countries have a trade "deficit" meaning they are losing more talent than they are acquiring. I want to see where the good players are going. The sketch will accomplish this by showing red and blue (colors can be changed) arrows indicating the exchange of talent in and out and where it's going. On the arrow will be the average rating sent in and out to the paired country, and I would love to include a timelapse mode that doesnt use user interaction and just shows where people have gone over the years in a timelapse format. I think it would be very cool to see animated arrows extending and disappearing, making way for new transfers.

## Open Questions

I'm interested in how to calculate the centroids from topoJSON.
I'm nervous about having too much going on in the viz, I think a timelapse would be super cool but it may get too busy.
I'm worried about scraping the FIDE website for historical ratings, I've never done this before.

## Schedule of Work

I was very behind schedule due to poor planning during A term, so I'm getting a late start to the iterative portions of the final project. The current work demonstrates what I intend to polish during the remaining
time of the course.

# 11/10/21 
Working with JSON data and understanding how to represent things I wanted to in D3, [Viz](https://vizhub.com/Patrick-Houlihan/4ef267da3ae848119fa321d5ce249896?edit=files), using the menus starter code used in an earlier viz assignment in the class, I was able to see what parts of my dataset were visually interesting and analyzed trends.

I also had to create my dataset. I made a website scraper to scrape the FIDE website for more data on Chess Transfers. The original dataset that inspired this can be found [here](https://gist.github.com/Patrick-Houlihan/601269a0a7811a08b1cd30f0e86aee1d)

I determined the dataset was too limiting earlier in the course, and I needed to find more information. Using the [FIDE website](https://www.fide.com/) and a [third party API](https://github.com/xRuiAlves/fide-ratings-scraper), I was able to expand the dataset from a url, a start federation, a destination federation, a date, and an ID, I was able to add the columns federation (the current federation), rating information to determine how skilled a player this person was, title information, ranking information for their current federation, continent, and worldwide ranks.

## Sample JSON Record
### {"ID": "2019221", "from": "Philippines", "to": "United States of America", "date": "12/15/00", "federation": "United States of America", "birth_year": 1961, "sex": "Male", "title": "FM", "standard_elo": 2369,
### "rapid_elo": 0, "blitz_elo": 0, "AllWRAP": 4385, "ActiveWRAP": 0, "AllNRAP": 246, "ActiveNRAP": 0, "AllActiveCAP": 578, "ActiveCAP": 0}

# 11/17/21
I moved to a new vizhub project on which I can better create a visualization of the data, [available here](https://vizhub.com/Patrick-Houlihan/d4be0f142c8e47ec8ccf952dfb358afa?file=bundle.js). This project combines the stylized scatterplot code used for the earlier project, without the menus, and adds the world map in basic D3 shown by Curran Kelleher earlier in the WPI Dataviz course. I added interaction via clicking a country and seeing the people with that country as their destination on the scatterplot below. In the next week I will polish this up to correctly match country to country and hopefully add more original components to the viz as well as menus for data filtering and selection.

# 12/1/21
I iterated on the existing vizhub project from last submission by mistake, [available here](https://vizhub.com/Patrick-Houlihan/d4be0f142c8e47ec8ccf952dfb358afa?file=bundle.js). This iteration includes the menus featured in the previous iteration and fixes some of the data problems with the United States not having the same TopoJSON name as the federation names by changing the dataset. Instead of featuring individual Federations for the United Kingdom countries, a United Kingdom Federation was added, conglomerating all players transferring to it.

# 12/9/21
I iterated on the existing vizhub project from last submission, as it was too large to create a new fork, [available here](https://vizhub.com/Patrick-Houlihan/d4be0f142c8e47ec8ccf952dfb358afa?file=bundle.js). This iteration adds both color mapping of selected countries and brush highlighting of countries. By selecting a region of points in the scatterplot, the countries selected can be highlighted. These highlighted countries are only the countries that appear as destinations in the subset highlighted by brushing. This can be used to see a subset of points based on rating score, to see where strong players are going. Each Scatterplot point matches the color of the originating country. This can be used to map regions like Europe and then compare values like Continetal Rating to see which European countries attract stronger players.
