---
title: 'From Data to Knowledge: Applying Schema Agnostic Systems Modeling to Development
  Challenges'
date: 2016-09-19 16:23:00 -04:00
published: false
---

By now the much vaunted “Big Data Revolution” that technologists have endlessly “touted” is in full swing. Hardly an industry or economic sector is not actively recognizing and harnessing the potential of digital data actively and passively collected from VARIOUS SOURCES. International Development is no different, as an ever increasing number of programs are being conceived with data for decision making as a central pillar to support improved intervention strategy, activity coordination, and impact measurement. This increased focus on data has lead to new technology-driven solutions for the collection and analysis of data for improved decision making.

There is little doubt about the value of many of the information systems being used to gather data, and transform that data to provide valuable information - From Health Information Systems such as DHIS2 to mobile data collection platforms such as the Open Data Kit (ODK). But while these platforms have helped us to effectively automate the collection of data and its transformation into actionable information, few systems address the question of how we might digitize and integrate actual expert knowledge into a system to further automate knowledge-based workflows. To better understand what this means, it is useful to understand the difference between data, information, and knowledge, and the Data, Information, Knowledge and Wisdom pyramid for data value extraction. The question at hand is: How can we in international development move from generating and collecting data and information to actually capturing knowledge - a human understanding of how complex systems work?

To explore this question, I recently contacted some old friends from Soley GMBH, a data analytics startup that specializes in just that - integrating expert knowledge into digital systems to automate resource-intensive workflows, and master complexity. Together we tried to come up with a use case that could demonstrate how their nifty modeling and simulation platform could help us understand how we might optimize farmer crop production in certain regions in Ethiopia to maximize farmer incomes. This was done by simulating a virtual crop marketplace in Ethiopia based on past market price and and localized climate data. The results were a set of recommendations for optimized crop production strategies for individual farmers in the market that would ensure farmers could maximize incomes in coming years just by planting an optimal combination of crops.

![Overview.png](/uploads/Overview.png)

Figure 1: A Virtual Cop Marketplace Model and Simulation in Soley Studio

## The process:

Let us pick pick apart how the good folks at Soley set up the model and came up with the optimal crop planting strategies for farmers. The first step was to create a so-called Meta-Model (sometimes referred to as an ontology or a schema) describing all the elements in the system and their interactions, specific to our use case.

Every Meta-Model contains a set of basic building blocks classified as either Nodes or Edges.

* **Nodes -** are entities within the model that often represent physical actors, goods, or services. In our model, nodes include:
  **1) Farmers                  2) Crops                   3) Traders**


* **Edges -** are the relationships that define how entities (or nodes) in the model interact with one another. In our model, edges include:

**         1)“Sells”                        2) “Buys”                   3) “are Competitors”**

Once a Meta-Model has been created, data from a variety of sources can be overlaid and mapped to the Meta-Model. The meta-model is dataset agnostic, meaning that any different datasets (from different countries for example) can be mapped to the same model. Elements and their relations can be queried as patterns (for example: farmer >> sells >> barley) so that the Meta-Model and the data sets are combined to create an actual working model. This intuitive approach is how an agent-based crop market was modeled.

![RecommendationGraph1.PNG](/uploads/RecommendationGraph1.PNG)

Figure 2: A graphical representation of a model that includes nodes (farmers, crops and traders) and edges (quantities of commodities sold and bought by farmer and traders respectively).

Finally - and perhaps most critically - the model includes a set and sequence of so-called “rules”. Defining rules allows for knowledgeable experts to integrate human understanding of complex subject matter that has been acquired through study and experience into the model. A simple example of such a rule could be that farmers aim to maximize profits by maximizing sales given specific commodity prices. But if this were the only rule encoded into the model, all farmers would simply produce a single crop - the crop with the highest market price - effectively leading to the depression of the market price, incurring greater farmer risk, and leading to farmers producing low-yield crops. So additional rules governing diversification for risk management (e.g. production of at least 2 crop varieties), as well as rules linking local climatic conditions (such as rainfall) to crop variety suitability were also encoded into the model. Finally, a rule governing the optimization of the combination of crop is included. These supply-side rules are then linked to demand data based on aggregate sales volumes of the previous year to link the supply side of the market to the demand side and link traders with to farmers.

![rules3.png](/uploads/rules3.png)

Figure 3:  Once rules have been defined, they are combined into sequences to run simulations

A market simulation is run based on sequences of rules (outlined above) to produce a new market scenario in which a group of farmers meet crop demands through an overall harmonization of crop production strategies.

The result of the simulation is a set of localized recommendations for farmers for which combination of crops to plant and harvest and at which quantities to optimize efficiency and income based on their local climate and market prices. In this model the suggested ratio of growing the best 2 crops are set to 80% and 20% of each farmer’s total amount. The suggestion itself refers to the amount of land that is supposed to be used to grow each crop as this information can be used easier by the farmers. This ratio could of course be adjusted or a third option could be suggested for each farmer in order to emphasis biological variety in the region.

The simulation of this crop production adjustment on the part of farmers in turn affects future market prices, based upon which the simulation can be iteratively run, until a market-clearing equilibrium is reached. Ultimately, the model reflects the fact that farmers’ incomes depend not only on the size of their land or the market price of the crops they produce, but a combination of that with environmental conditions such as humidity and altitude, and enable macro-level modeling of complex systems to yield localized, specific recommendations for crop optimization based on specialized expertise.

While this particular model that Soley built doesn’t reflect all the elements and relationships required to manage an entire crop market, the simple use-case demonstrates the potential of schema-agnostic data modeling platforms that can use readily available data and a limited set of expertise-based rules, to provide insight into creating more sustainable and productive markets, whether in agriculture or elsehwere.

Paragraph 7: More Info on Soley - Links
Soley’s Mission is “Empowering Experts” in the sense of enabling people to use their knowledge to improve their situation, to become more productive and win valuable insights. The international team created a powerful data analysis framework with a focus on usability and transparency when it comes to mastering complexity. With an academic alliance and open source analysis applications in different domains, Soley empowers not only students of using powerful data analysis, but cooperates with universities, consultancies and other organizations in order to develop individualized easy to customize analysis solutions. Their development environment Soley Studio is used to create analysis workflows that can be spread using the desktop application Soley Desk or the browser-based Soley Web-Desk. The Idea to multiply expertise by digitalizing and sharing expert knowledge has the potential to spread knowledge not only throughout companies, but also countries and continents.
Whoever want’s to get a detailed impression on how Soley Studio works, can download the Software 30-Days-Trial, and visit one of the free Workshops. As the Software is designed to run even on a Laptop, starting powerful analysis is not a matter of technical infrastructure any more and can work from highly decentralized infrastructure up to enterprise solutions.