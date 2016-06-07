# Treasure Finder! Never Buy Again!
This is a bot which scrapes free stuff from craigslist. It's written in python 3.x but ought to be compatible with 2.x (once you change the print/input functions accordingly).

- Using the first two scripts, Stuff  and Stuffify, one can gather together the most recent freestuffs off craigslist, meaning the 
Title, Location, Image, and URL. into a a list of stuff, stuffs[ ]. 
- Using Mappify, one can post the freestuffs, and geolocalize them, onto a leaflet map.
- With tweetstuffs and shortenurl, one can post free stuffs onto Craigslist (shortenurl is not needed for twitter anymore).

## The "Twitter" Branch is for posting freestuffs onto twitter. 
Horay! New York is the pilot project.
- It posts pictures!

### To run freestuff-bot and use the mappify module, first run <code>python -m http.server</code>
### Example:
* <code>stuffs = Stuffify("montreal", 10, precise=True).get_freestuffs()</code>
* <code>mappify.post_map(stuffs)</code> 

<b>The findit.html file is an example of the map output.</b> It can be nicely embedded in a Jinja2 app. See my  [treasure-map](https://github.com/polypmer/treasure-map).

### Main Dependencies:
<ul>
<li>requests</li>
<li>geopy</li>
<li>folium</li>
<li>BeautifulSoup4</li>
</ul>

### So much todo (planned features & broken features):
<ul>
  <li>Woah, daemon sync in the background: https://github.com/serverdensity/python-daemon</li>
  <li>Add contact info? [This is harder than it seems...]</li>
  <li>Package it?</li>
  <li>Continue to refine location methods/folium tricksss</li>
  <li>put <code>python -m http.server</code> in the init... Is this possible? Or as a map feature?</li>
</ul>

