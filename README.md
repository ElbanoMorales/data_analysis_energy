# Trends and insights on energy consumption.
## Elbano Morales. 2022-08-06.

In order to finish my Google Data Analytics Certificate, I chose as my Case Study to find some trends and insights about our current global energy consumption, which I would like to share with you. All calculations and graphics were done using #R in #RStudio, except for the world map graph, which was made in #Tableau. To clean and combine two different datasets I used #SQL in #BigQuery. I used point symbols for decimal places and comma symbols for thousands.

Being a #dataanalyst, I analyze, discuss and make claims from a data-driven perspective. We will start our journey by seeing past and present energetic demands and our current energetic sources. We will explore different countries’ energetic habits and how efficient they are. After sharing some personal thoughts about energy policies, I’ll try to answer the last and most important question of this analysis: can we live a happy and prosperous life and save energy at the same time?

In a daily basis, humans expend energy for agriculture, shelter, transportation, health, just to name a few. How much energy do we consume? My first source is **bp’s** “Statistical Review of World Energy 2022 – 71st edition”, whose data ranges from 1965 to 2021. In 2021, we consumed 595.15 Exa Joules of primary energies. I did the search for us, Exa stands for 10^18, a really big number: one million of one million of one million. Primary energies includes both renewables and non-renewables.

If we take into account that we were around 7,872 million humans in 2021, we get that we consumed 75.6 Giga Joules per capita. To see it in another perspective, that was about 49,500 Calories *per day* per capita and, if an average person should eat some 2,000 Calories a day to meet standard requirements, it gives that each one of us had a daily energetic expense 25 times bigger than our metabolic necessity.

Are we consuming more energy these days than previous years? In 1965 we consumed 156 Exa Joules of primary energies so, yes, we basically consume 4 times more energy nowadays. Naturally, our population has grown a lot in more than 50 years but, is our energy consumption more related to our population size or to our population behavior? Let’s see what data has to say about it in Figure 1.

![img](https://drive.google.com/uc?id=1GtWV0mY-19MWoZgepAjrTIkomJQK9qDZ)

This graph shows our yearly global energetic demand per capita. We can see an increasing trend, which allows us to elaborate on two ideas in order to gain our first insight. The first idea is that the trend is clear, there is a good correlation coefficient of 0.934. This means that both variables are well related. For those who need to know, the correlation coefficient is a statistical value that ranges from -1 to 1 and shows how well two variables are related. Values close to 0 indicate that the variables are not related at all, and values closer to -1, or to 1, indicate that they are strongly related. The second idea comes from that this trend could be constant, or could even decrease, but it increases. Based on this, the first insight is that **we tend to consume more energy with time, not (only) because our population grows, but because of our behavior**. Remember that in 2021, mathematically speaking, each person demanded about 49,500 Calories every day? Well, in 1965, each person demanded 30,500 Calories. That’s a good 50% increase.

Naturally, countries with bigger population sizes should consume more #energy than countries with lower population sizes, or not? In Figure 2, we plot each country’s population size against their energy consumption of 2021.

![img](https://drive.google.com/uc?id=1Dm6_UN-ggvRklIxOC7oKAfCg3hni4RdT)

This is a very interesting graph. The correlation coefficient is R=0.78, which tells us that the variables are somewhat related. At first glance we could say that generally, larger population sizes carry with bigger energy consumption, but I will explain why we should be careful with this statement.

Except for four, all data points are scattered inside an area that ranges from 0 to less than 25 EJ and from 0 to around 250 million inhabitants. Outside this area, from left to right we find Russia, India, United States and China. There is barely no data between the leftmost data cloud and the rest of the domain to confirm a good trend or behavior. More specifically, we have a sample of 79 countries and a domain up to 157 EJ which means that 95% of data points are gathered in less than 15% of the domain. Take, for example, Russia and India. They consumed almost the same amount of energy (30 and 34 EJ, respectively), but they had very different population sizes: Russia had 145 million and India 1,368 million people. Parallel to this idea, China and India had almost the same population size but spent really different amounts of energy, and The United States had twice the population size of Russia but spent three times more energy. To make things worse, the data cloud on the left does not seem to have any clear trend by itself.

We shall conclude that despite they are somewhat related, a country’s energetic consumption is not directly related to its population size, if not, we would find a relative narrow range of countries’ energetic consumption per capita. How wide is this range? Which countries consumed the most energy per capita in 2021? Which countries have increased their energetic consumption per capita since 1965 above the 50% global average? Are there any countries that decreased it?

To address these questions let’s find in Figure 3 the primary energies consumption per capita of 2021. Per capita consumption ranges from 4.7 to 686 GJ. Would you guess who tops the list? The top ten countries are Qatar, Singapore, Iceland, United Arab Emirates, Trinidad & Tobago, Kuwait, Norway, Canada, Oman and Saudi Arabia. Yes, make no false guesses, no China, United States, India, Russia or Japan, who are the countries that in gross consumed the most energy in 2021 (in that order). Qatar and Singapore are virtually invisible at a global scale. This wide range confirms our suspicion that **a country’s energetic consumption is not necessarily proportional to its population size**.

![img](https://drive.google.com/uc?id=1Otjf2eR_pXNT4xEyjzuxOJVltf4QI9jg)

From 1965 to 2021, there were 45 countries that increased their per capita energetic consumption more than the 50% global average, which can be found in Figure 4. Regions with more participation are the Middle East, Europe and Asia Pacific. Six countries grossed the 1,000% mark, with Oman even reaching 58,600%. The bulk majority falls between the 100% and 1,000% range.

![img](https://drive.google.com/uc?id=1_qYraC9Mw2nJfkeDi6Nt5iQxnXxcknNg)

On the other side of the story, countries that decreased their per capita energetic consumption in this period were Venezuela (-0.49%), Denmark (-8.56%), Czech Republic (-8.98%), United Kingdom (-30.38%), Kuwait (-33.38%), and Luxembourg (-48.51%). I found these facts very interesting, would you have guessed what these countries had in common?

Now that we have a clearer view of our energetic demands, we can ask ourselves, where does all of our energy currently come from? In a more specific way, which were the sources of energy that made up the 595.15 EJ that we used in 2021? They are all illustrated in Figure 5.

![img](https://drive.google.com/uc?id=1wC_XAzyRy1Vdj-xD8sSM-YR6fR6L77W1)

In 2021, 82% of our primary energies came from fossil sources, #nuclear energy helped with 4.3%, #hydroelectricity with 6.8% and the remaining 6.7% belonged to #renewable sources (like #solar and #eolic). Also, last year we emitted almost 34.000 million tons of carbon dioxide and, as a #petroleum engineer, I want to address this delicate matter with much respect.

At first, we might think that fossil energies are the ones to blame for our carbon dioxide emissions and yes, there is a direct causation and relationship between them, but fossil energies are just the means we use to reach our energetic -yearly increasing- demands. Given what #data has shown us so far, I like instead to think that our own behavior is more responsible for our current carbon footprint. Is fossil energy preventing us to lower our carbon dioxide emissions? Consumption of other sources of primary energies have greatly increased in the last years; you can find their performance in Figure 6. Still, far from dropping, our carbon dioxide emissions have kept their steady pace: on average, every year we generate 405 million more tons of carbon dioxide than the previous one.

![img](https://drive.google.com/uc?id=1bvYKK94DbDoDkqCfGXGlvlCiRdzWOn1d)

There are several myths around energy policies which have been both promoted and criticized through the years by “subject matter experts”. These topics are appropriately addressed by Vaclav Smil in his book “Energy myths and realities”. I personally find it counterproductive both to promote or discourage any energy option without substantial knowledge of the processes involved. Yes, electric cars are a good alternative, but where does the electricity needed to charge them would come from? Yes, there have been negative nuclear experiences, but it doesn’t mean nuclear energy is an unsafe option. Returning to #fossil energies, it would be inappropriate to blame or cancel these fundamental sources that have allowed us to enjoy so much life quality improvement and technological advances. I think energy policies should be clear and realistic, with a diversified and varied portfolio of energy sources.

Public misconceptions help us forget about one fundamental part to approach our carbon dioxide problem: personal habits on energy saving. These are the final questions of this analysis: Can we live a happy and prosperous life saving energy at the same time? If we care too much about our energy habits and try to be more efficient, would we produce less wealth? Is energy consumption a fundamental requisite for wealth generation?

To find these final answers we will use the Gross Domestic Product of each country found in our second source, The United Nations’ Department of Economic and Social Affairs, Statistics Division, National Accounts. As a comment, this dataset had some countries whose names differed from the ones on the first dataset so, some querying was used in BigQuery to identify and rematch country names before analysis.

We need to know if someone around the world was able to make money and save energy at the same time. To do so, through Figure 7 we will evaluate Gross Domestic Product per capita vs. Primary Energies Consumption in 2019. There, we can see the total energy a country spent and the amount of money each one of its citizens gained. Please bear in mind that the following analysis doesn’t reflect the reality of every individual, but the reality of the average.

![img](https://drive.google.com/uc?id=1xlj6nGJn8KejeRtqNF7BYx-i322TLJC4)

This time, there is a wide range of data scattered in the same small domain so there is no correlation between variables, which means that in 2019, there were countries with the same energy expenditure and whose citizens produced considerably different amounts of money. Looking at it the other way, there were countries whose citizens needed distinct energy quantities to earn the same money. Of course, wealth generation is a complex function of several variables like domestic policies, foreign relationships, mineral resources, geography, climate, soil conditions, biodiversity, etc., and we are analyzing merely from an energetic perspective.
 
Yet, what I like to keep from this is that **we can adopt ways of being both productive and energy efficient at the same time** and, if we do, we could lower our #carbonfootprint without compromising our life quality. Personally, this is the most important insight I found from this #dataanalysis.

Which countries were more efficient? We could calculate a metric with these variables that represent the income each person had in 2019 for every unit of energy they spent. The higher the value, the more money someone made out of every Joule. Figure 8 has a summary of this metric.

![img](https://drive.google.com/uc?id=1qKbSnIv0vLPtEznoAg-Lmqfp0Qqdy3dn)

We see the same variety of values from Figure 7. Just to name 2 examples, a New Zealand citizen makes more than $200 out of every Giga Joule and, in my country Venezuela, for each Giga Joule spent each one of us earns around $75. Again, far from judging any country’s policies, what I want to leave is that energetically speaking, there are different ways of making money. I’ll leave you as a closing gift a similar graph that relates how much money each citizen earns out of every ton of #co2 in Figure 9.

![img](https://drive.google.com/uc?id=1rUZdjBbmO1zMAZftUYmewCwmjhJ5XcvS)

As a final reflection, if we achieved to adopt more efficient ways of handling energy, would we still lower our total consumption? So far, we know we tend to increase our demands with time, maybe that could change if we made some behavioral changes, but not necessarily with more efficient ways of handling energy. Back in 1865, William Jevons published his book “The Coal Question”, in which he treated the United Kingdom’s coal consumption. He noted that when more efficient coal engines were invented, coal demand rallied. He explained that more efficient ways of handling a resource, far for lowering its demand, increases it. I think I agree with this logic. Imagine you could buy a plane ticket ten times cheaper. You could go to that desired destination, or see that desired person, ten times easier. Would you still fly the same number of times and save the gains? Maybe, maybe not.
