# tennis-draws

Generates a graphic representation (an SVG file) of singles draws and results for top tier professional tennis tournaments
using data from the [Sportradar Tennis v3 API](https://developer.sportradar.com/docs/read/tennis/Tennis_v3).
Here are some [examples](https://donald.net.au/tennis) of documents produced using this application.
To convert SVG files to PDF I recommend [Boxy SVG](https://boxy-svg.com/).

To use this application, you’ll first need to register an account with Sportradar and get a trial API key.

Download the code and install the packages upon which it depends:

    npm install

Executing the code requires parameters as follows:

    node index.js tournament_code year event_code stage_code api_key [show_timestamp]

Valid values for `tournament_code`:

* __ao__ — Australian Open
* __iw__ — Indian Wells
* __mi__ — Miami Open
* __ma__ — Madrid
* __ro__ — Rome
* __rg__ — French Open
* __wi__ — Wimbledon
* __ca__ — Canadian Open
* __ci__ — Cincinnati
* __us__ — US Open

Valid values for `event_code`:

* __ms__ — Men’s Singles
* __ws__ — Women’s Singles

Valid values for `stage_code`:

* __q__ — Qualifying
* __m__ — Main Draw

Valid values for `show_timestamp`:

* __y__ — Include the current timestamp on the generated draw sheet (default)
* __n__ — Do not include the current timestamp

If you are testing adjustments to the code, you can regenerate the SVG file without calling the API every time, because
the parameters and API results are cached locally. To regenerate the SVG file from local cache, just execute without parameters:

    node index.js

The code embeds Sportradar’s identifiers for recent tournaments. If you want to extend the code to include additional tournaments/events, you’ll need to add __season__ identifiers to the code. 
In the Sportradar API, a __competition__ is an event at a tournament, eg "Australian Open Women’s Singles", and a __season__ is an individual occurrence of an event, eg "Australian Open Women’s Singles 2022".
You can call the API endpoints [Competitions](https://developer.sportradar.com/docs/read/tennis/Tennis_v3#competitions) and [Competition Seasons](https://developer.sportradar.com/docs/read/tennis/Tennis_v3#competition-seasons) to discover season identifiers.

