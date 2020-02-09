# Dependency Charts

This article serves two purposes.
The first is to present the main ways I've seen item/lock/key dependencies documented and designed in games.
The second is to muse on and present some ideas about a new kind of graph that captures the best elements of them all.

My hope is that we, as a community, can collectively can stand on the shoulders of giants and lift everyone a little higher.

## Ron Gilbert Style Charts

> For context, check out Ron Gilbert's [post on his blog](https://grumpygamer.com/puzzle_dependency_charts) about how he created and used these charts.

### Gilbert Chart Elements

### Gilbert Chart Specific Insights

Below is a chart of all of the key item dependencies required to beat *Ocarina of Time*.
It's extremely valuable in documenting the flow of events throughout the game as a whole without getting caught up in the details of dungeons and story elements.

> **NOTE**: Gareth Rees, the author of this chart, added some structure by placing dependencies above and below one another.
> Things lower on the chart are dependent on the things above them.
> It makes the graph easier to read with so many elements.

<!-- ![Ocarina of Time Item Graph](/images/202002041230-ootReesItemGraph.png) -->

Image from *[Puzzle Structure of Ocarina of Time](https://garethrees.org/2004/12/01/ocarina-of-time/)* by Gareth Rees on [garethrees.com](https://garethrees.org/2004/12/01/ocarina-of-time/)

## Mark Brown (GMTK) Style Charts

> Before you dive into my description of them, check out Mark's [detailed description about how his charts work](https://www.patreon.com/posts/how-i-make-graph-20631617).

Mark Brown's charts are cool in that the structure of the chart itself conveys more information than a more flexible chart can.
For example, in Ron Gilbert's charts above, the fluid nature of where elements are placed makes it difficult to quickly scan the chart to gain meaningful information.
It acts more as documentation than it does as a tool to be read.

Mark's charts, in contrast, are built with a specific goal in mind, and that limitation allows for quick parsing.
They originally started as a graph to map out the key/lock dependencies in the *Zelda* games.
As such, they are heavily influenced by how those games tend to use keys and locks.

### GMTK Chart Elements

A ***lock*** can be more generally thought of as a designer imposed obstacle.
Locked doors obviously fit into this category, but can include less obvious things like switches that are activated by being shot with an arrow.
Or a ledge that can only be scaled with a new power-up.

A ***key*** is the thing that allows you, as the player, to bypass a particular ***lock***.
To use those same examples, a small key would open a typical door.
A bow and arrow would be a 'key item' that allows you to shoot the lock with the required arrow.
And the ledge could be scaled via a double-jump powerup.

Because everything is simplified into a set of ***locks*** and ***keys***, the chart can be optimized to focus on surfacing the relationships between them.
And herein lies the brilliance of Mark's charts.
Rather than allowing the elements to float freely, he uses vertical and horizontal positioning of the elements to convey additional information.

### GMTK Chart Specific Insights

It easy to quickly scan and parse a graph to understand the relative linearity and backtracking required to solve a physically based set of lock/key puzzles.

I recreated Gareth Rees' item dependency chart using Mark Brown's chart structure, and it's already easier to read (if not a little taller).
Of note is how easy it is to see how linear the game is at first, but quickly opens up when you become an adult.
Then you can see the game narrow down slowly until it becomes linear toward the end.

<!-- ![Mark Brown Style Ocarina of Time Item Graph](/images/202002041236-ootGMTKGraph.png) -->

## Petri Nets

> Petri Nets are a relatively niche chart in the mathematics community used for modeling concurrent distributed systems.
> Check out the [article on Wikipedia](https://en.wikipedia.org/wiki/Petri_net) about them.

There are some really cool things that make Petri Nets *almost* ideal for modeling game structures.
However, their rigid elements can sometimes make simple game designs look unwieldy, and also lack some basic functionality that could help.

They also suffer from the same problem as Gilbert's charts, namely that their flexibility can make a chart feel like a mass of lines rather than something useful to parse quickly.
They're better at documenting literal systems than they are at quickly comparing and analyzing different systems.

### Petri Net Chart Elements

Petri Nets are have four specific elements:

1. State Marker (Circle)
1. Transition Marker (Rectangle/Bar)
1. Input Arc (Into a Transition)
1. Output Arc (Out of a Transition)
1. Places (Dots inside the State)

These four elements can make some fairly robust concurrent system graphs.

### Petri Net Chart Specific Insights

What I find really cool about them is the way the elements have one-to-one correlations with the building blocks of games.

It's been said that games are a bunch of verbs. <!-- todo: need citation -->
So, an easy correlation could be:

1. States -> States
1. Transitions -> Verbs
1. Arcs -> connections between them

So a player character's move set can be modeled using a series of States and Verbs keeping track of the different states via the places stored within the state circles.

Or the items in a map could be represented via a series of states, as well as the player character's position in the physical space.
The key/lock paradigm that is the focus of Mark Brown's graphs can be modeled as well.

Essentially, Petri Nets could be a very powerful way to model and keep track of a lot of information.

<!-- TODO: talk about limitations and colored nets -->

> **NOTE**: I started to recreate Rees' chart as a Petri Net, but it became unwieldy quickly.
> The benefits of using a vanilla Petri Net in this case are negligible.
> It looked essentially the same, but had twice the number of nodes.
> Petri Nets could maybe help model inventory collection, or multiple concurrent players.

## My Hybrid Charts

I really like the robustness of Petri Nets in comparison to Ron Gilbert's more generalized 