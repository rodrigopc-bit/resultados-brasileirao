# Brasileirao fixture predictions
Predicts the results of Campeonato Brasileiro's fixtures, using Naive Bayes

## Requirements
First, you need to make sure you have Python3 installed on your computer. To do this, simply go to your terminal or command prompt and write `python`, then hit Enter e see if prompts Python. If it doesn't, go to [Python website](https://www.python.org/downloads/) and download the latest version of Python3. After installing python, open your terminal/command prompt again and write `pip install jupyterlab`. This will download and install JupyterLab, which will be important since the script is currently made using jupyterlab's notebooks.

## How to use
Download the [Resultados_Brasileirao.ipynb]() and open it using the JupyterLab's notebooks. You should see three arrays:
1. `equipeCasa[]` - Home teams, with each line representing 1 fixture
2. `equipeFora[]` - Away teams, with each line representing 1 fixture
3. `resultadoPartida[]` - Results of each match. The results can be passed as Vitoria (Victory), Empate (Draw) or Derrota (Defeat) and they're always based on the Home Teams, meaning if the Away Teams wins, you should pass as Derrota (Defeat), since that means the Home Team lost the match.

The index of each array represents 1 match, so if you want to pass the following result: São Paulo 3 x 1 Palmeiras, you should pass it in the same index for all the arrays.
In the file, the first 10 fixtures of Campeonato Brasileiro 2022 are already coded, so you can use it as an example.

Now, this is just for de input data. For the prediction part, you need to use the numbers of the teams. Each team has an unique number, which is how the algorithm "sees" each team. It automatically atributes a number to the team, going from 0 to n-1 (n being the number of different teams passed to the algorithm). This atributtion is done by alphabetical order.

Using Campeonato Brasileiro 2022, the teams numbers are:
<br> 0 - America-MG
<br> 1 - Athletico-PR
<br> 2 - Atletico-GO
<br> 3 - Atletico-MG
<br> 4 - Avai
<br> 5 - Botafogo
<br> 6 - Bragantino
<br> 7 - Ceara
<br> 8 - Corinthians
<br> 9 - Coritiba
<br> 10 - Cuiaba
<br> 11 - Flamengo
<br> 12 - Fluminense
<br> 13 - Fortaleza
<br> 14 - Goias
<br> 15 - Internacional
<br> 16 - Juventude
<br> 17 - Palmeiras
<br> 18 - Santos
<br> 19 - Sao Paulo

Go to "predicao" and pass the teams playing in the fixture you want the algorithm to predict. So, a match between Fortaleza and Ceara, should be passed as `[13, 7]`
The result will be either 0, 1 or 2, meaning:
0. Defeat of the home team
1. Draw
2. Victory of the home team

So, in our example, 0 means Ceara wins, 1 means draw and 2 means Fortaleza wins.

You can pass more than one match at a time, by separating them with a comma (,).
