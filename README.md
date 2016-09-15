# A shiny app to simulate infectious disease in a network 

This is a shiny app for visualizing the spread of SIR-like infectious disease in a network. 

The app allows you to customize the network and disease dynamic. The underlying algorithm uses an agent based model to simulate the disease progression. The app displays an animation of disease progression in the network, and summary plots of the S-I-R compartment size over time. 

## Screenshots


<p align="center">
  <img src="screenshot1.png" width="700"/>
  <img src="screenshot2.png" width="700"/>
</p>

## Usage

You will need RStudio and internet connection to run the app. Click [here](https://www.rstudio.com/home/) to install RStudio.

To launch the app, open RStudio and run the following code. 

```R
# install shiny package if not done
# install.packages("shiny")

library(shiny)

runGitHub("shiny-SimNetwork","alisonswu")
```

## Documentation
We use the [R igraph](http://igraph.org/r/) package to generate a graph representation of network. Each vertex of the graph represents an individual in the network, and the edge between two vertices represents physical contact between the individuals. 

<p align="center">
  <img src="graph.png" width="200"/>
</p>

We use an agent-based model to simulate an SIR-like infectious disease over discrete time points (t). The inividuals in the network can have one of the three status: S(susceptible), I(infected), R(recovered). 
At t = 1, initiate the network with a small subset of infected individuals, while the remaining are susceptible.
At t = 2,3,... 
A suscpetible individual becomes infected with probability

An infected individual become recovered after staying infected over the infection duration.
A recovered individual remains recovered.  










