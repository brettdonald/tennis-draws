# tennis-draws

Generates a graphic representation (an SVG file) of singles draws and results for the four major tennis tournaments: the Australian Open, Roland Garros, Wimbeldon and the US Open, using data from the [Sportradar Tennis v3 API](https://developer.sportradar.com/docs/read/tennis/Tennis_v3). Here are some [examples](https://donald.net.au/tennis) of documents produced using this application.

To use this application, you’ll first need to register an account with Sportradar and get a trial API key.

Then you’ll need the identifier of the __season__ you want to generate a draw for. In the Sportradar API, a __competition__ is an event at a tournament, eg "Australian Open Women’s Singles", and a __season__ is an individual occurrence of an event, eg "Australian Open Women’s Singles 2021". You can call the API endpoints [Competitions](https://developer.sportradar.com/docs/read/tennis/Tennis_v3#competitions) and [Competition Seasons](https://developer.sportradar.com/docs/read/tennis/Tennis_v3#competition-seasons) to discover the relevant season identifier. Or you can try one of these identifiers from 2021:
<br><br>
<table>
  <tr><td>Australian Open 2021 Men’s Singles</td><td>sr:season:75673</td></tr>
  <tr><td>Australian Open 2021 Women’s Singles</td><td>sr:season:75675</td></tr>
  <tr><td>Roland Garros 2021 Men’s Singles</td><td>sr:season:79241</td></tr>
  <tr><td>Roland Garros 2021 Women’s Singles</td><td>sr:season:79267</td></tr>
  <tr><td>Wimbledon 2021 Men’s Singles</td><td>sr:season:76843</td></tr>
  <tr><td>Wimbledon 2021 Women’s Singles</td><td>sr:season:76845</td></tr>
  <tr><td>US Open 2021 Men’s Singles</td><td>sr:season:78537</td></tr>
  <tr><td>US Open 2021 Women’s Singles</td><td>sr:season:78539</td></tr>
</table>
<br>
Download the code and install the packages upon which it depends

    npm install

Executing the code requires five parameters as follows:

    node index.js ao|rg|wi|us year m|w season_id api_key

The first three parameters are used to generate the title lines rendered into graphic. The fourth and fifth parameters are used to call the API.
