[XSS-Game](https://xss-game.appspot.com/)
=========================================

Hint and Solution to [XSS Game on Appspot](https://xss-game.appspot.com/)

Level 1
-------

**Hint**

The textbox will include any html in page including tags.

**Solution**

Type `<script>alert("GG")</script>` and it will give you the popup.

Level 2
-------

**Hint**

If you read the hints of the level, then you should already know what to do

**Solution**

Use the `<img />` tag and its `onerror` attribute. `<img src="forbidden" onerror="alert('GG')" />`
