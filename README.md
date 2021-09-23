# Data Visualization Project

## Data

The data I propose to visualize for my project is chess transfers from country to country between 2000 and 2017

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

The idea for this sketch is a world map, HOPEFULLY a globe since 2D maps are weak (per this week's lecture) that you can click on a country and it will show you all the transfers to and from that region. Chess is a very nationalistic game at times, see the Cold War for examples of that, and some regions are significantly strongers than others. I'm curious to see how average transfered rating (skill level applies to chess). I want to see what countries have a trade "deficit" meaning they are losing more talent than they are acquiring. I want to see where the good players are going. The sketch will accomplish this by showing red and blue (colors can be changed) arrows indicating the exchange of talent in and out and where it's going. On the arrow will be the average rating sent in and out to the paired country, and I would love to include a timelapse mode that doesnt use user interaction and just shows where people have gone over the years in a timelapse format. I think it would be very cool to see animated arrows extending and disappearing, making way for new transfers.

## Open Questions

I'm interested in how to calculate the centroids from topoJSON.
I'm nervous about having too much going on in the viz, I think a timelapse would be super cool but it may get too busy.
I'm worried about scraping the FIDE website for historical ratings, I've never done this before.
