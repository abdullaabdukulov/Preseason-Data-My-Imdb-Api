<div class="card-block">
<div class="row">
<div class="col tab-content">
<div class="tab-pane active show" id="subject" role="tabpanel">
<div class="row">
<div class="col-md-12 col-xl-12">
<div class="markdown-body">
<p class="text-muted m-b-15">
</p><h1>My Imdb Api</h1>
<p>Remember to git add &amp;&amp; git commit &amp;&amp; git push each exercise!</p>
<p>We will execute your function with our test(s), please DO NOT PROVIDE ANY TEST(S) in your file</p>
<p>For each exercise, you will have to create a folder and in this folder, you will have additional files that contain your work. Folder names are provided at the beginning of each exercise under <code>submit directory</code> and specific file names for each exercise are also provided at the beginning of each exercise under <code>submit file(s)</code>.</p>
<hr>
<table>
<thead>
<tr>
<th>My Imdb Api</th>
<th></th>
</tr>
</thead>
<tbody>
<tr>
<td>Submit directory</td>
<td>.</td>
</tr>
<tr>
<td>Submit file</td>
<td>app.py</td>
</tr>
</tbody>
</table>
<h3>Description</h3>
<h2>Description</h2>
<p>Ohhhh nooo!! IMDB just went down. Luckily we heard that you could help to provide a <code>service</code> while IMDB's DevOps team gets the website back online.</p>
<p>You will create a backend API to allow a user to search for a movie search by genre.
What is a backend? What is an API?
These two questions might require some googling to grasp the concepts before starting the project. :-)</p>
<p>We will provide you with a <a href="https://storage.googleapis.com/qwasar-public/track-ds/imdb-movie-data.csv" target="_blank">CSV</a> file.
This file contains more than one thousand movie titles. One of the columns marks the genre for each movie.</p>
<p>Your backend will receive a requested genre and will only <code>serve</code> movies with the corresponding <code>genre</code>.
Example:
The client requests all Action movies.
Your backend should parse the CSV, filter by the genre `Action and reply with a list of Action movies, while also respecting the HTTP protocol.</p>
<p>For this project you will be able to use a <code>framework</code> to take care of the HTTP communication protocol.</p>
<h2>Technical Description</h2>
<p>Create a backend app with a light web framework. (For python we recommend using <code>flask</code>.)
It will <code>listen</code> on port 8080.</p>
<p>All your routes will answer in <code>JSON</code> format!</p>
<p>You don't need to create a database, just parse the provided <a href="https://storage.googleapis.com/qwasar-public/track-ds/imdb-movie-data.csv" target="_blank">CSV</a>.</p>
<p>Your backend will serve six <code>routes</code>:</p>
<ul>
<li>
<code>GET</code> on <code>/</code>
This route will parse the GET parameter <code>genre</code>, to be able to filter by movie genre.</li>
</ul>
<p>Example on how to access this route:</p>
<pre class=" language-plain"><code class=" language-plain">curl "http://localhost:8080?genre=action"
</code></pre>
<ul>
<li>
<code>GET</code> on <code>/action</code>
This route will only serve action movies.</li>
</ul>
<p>Example on how to access this route:</p>
<pre class=" language-plain"><code class=" language-plain">curl "http://localhost:8080/action"
</code></pre>
<ul>
<li>
<code>GET</code> on <code>/adventure</code>
This route will only serve adventure movies.</li>
</ul>
<p>Example on how to access this route:</p>
<pre class=" language-plain"><code class=" language-plain">curl "http://localhost:8080/adventure"
</code></pre>
<ul>
<li>
<code>GET</code> on <code>/comedy</code>
This route will only serve comedy movies.</li>
</ul>
<p>Example on how to access this route:</p>
<pre class=" language-plain"><code class=" language-plain">curl "http://localhost:8080/comedy"
</code></pre>
<ul>
<li>
<code>GET</code> on <code>/drama</code>
This route will only serve drama movies.</li>
</ul>
<p>Example on how to access this route:</p>
<pre class=" language-plain"><code class=" language-plain">curl "http://localhost:8080/drama"
</code></pre>
<ul>
<li>
<code>GET</code> on <code>/romance</code>
This route will only serve romance movies.</li>
</ul>
<p>Example on how to access this route:</p>
<pre class=" language-plain"><code class=" language-plain">curl "http://localhost:8080/romance"
</code></pre>
<p>Example:</p>
<pre class=" language-plain"><code class=" language-plain">[my_imdb_api/]curl "localhost:8080?genre=western"
[{"Rank":"39","Title":"The Magnificent Seven","Genre":"Action,Adventure,Western","Description":"Seven gunmen in the old west gradually come together to help a poor village against savage thieves.","Director":"Antoine Fuqua","Actors":"Denzel Washington, Chris Pratt, Ethan Hawke,Vincent D'Onofrio","Year":"2016","Runtime (Minutes)":"132","Rating":"6.9","Votes":"122853","Revenue (Millions)":"93.38","Metascore":"54"},{"Rank":"140","Title":"Brimstone","Genre":"Mystery,Thriller,Western","Description":"From the moment the new reverend climbs the pulpit, Liz knows she and her family are in great danger.","Director":"Martin Koolhoven","Actors":"Dakota Fanning, Guy Pearce, Kit Harington,Carice van Houten","Year":"2016","Runtime (Minutes)":"148","Rating":"7.1","Votes":"13004","Revenue (Millions)":null,"Metascore":"44"},{"Rank":"145","Title":"Django Unchained","Genre":"Drama,Western","Description":"With the help of a German bounty hunter , a freed slave sets out to rescue his wife from a brutal Mississippi plantation owner.","Director":"Quentin Tarantino","Actors":"Jamie Foxx, Christoph Waltz, Leonardo DiCaprio,Kerry Washington","Year":"2012","Runtime (Minutes)":"165","Rating":"8.4","Votes":"1039115","Revenue (Millions)":"162.8","Metascore":"81"},{"Rank":"643","Title":"The Ridiculous 6","Genre":"Comedy,Western","Description":"An outlaw who was raised by Native Americans discovers that he has five half-brothers; together the men go on a mission to find their wayward, deadbeat dad.","Director":"Frank Coraci","Actors":"Adam Sandler, Terry Crews, Jorge Garcia, Taylor Lautner","Year":"2015","Runtime (Minutes)":"119","Rating":"4.8","Votes":"31149","Revenue (Millions)":null,"Metascore":"18"},{"Rank":"744","Title":"True Grit","Genre":"Adventure,Drama,Western","Description":"A tough U.S. Marshal helps a stubborn teenager track down her father's murderer.","Director":"Ethan Coen","Actors":"Jeff Bridges, Matt Damon, Hailee Steinfeld,Josh Brolin","Year":"2010","Runtime (Minutes)":"110","Rating":"7.6","Votes":"254904","Revenue (Millions)":"171.03","Metascore":"80"},{"Rank":"746","Title":"A Million Ways to Die in the West","Genre":"Comedy,Romance,Western","Description":"As a cowardly farmer begins to fall for the mysterious new woman in town, he must put his new-found courage to the test when her husband, a notorious gun-slinger, announces his arrival.","Director":"Seth MacFarlane","Actors":"Seth MacFarlane, Charlize Theron, Liam Neeson,Amanda Seyfried","Year":"2014","Runtime (Minutes)":"116","Rating":"6.1","Votes":"144779","Revenue (Millions)":"42.62","Metascore":"44"},{"Rank":"970","Title":"The Lone Ranger","Genre":"Action,Adventure,Western","Description":"Native American warrior Tonto recounts the untold tales that transformed John Reid, a man of the law, into a legend of justice.","Director":"Gore Verbinski","Actors":"Johnny Depp, Armie Hammer, William Fichtner,Tom Wilkinson","Year":"2013","Runtime (Minutes)":"150","Rating":"6.5","Votes":"190855","Revenue (Millions)":"89.29","Metascore":null}]
[my_imdb_api/]
</code></pre>
<p>You can also write a section inside your README.md on <code>how-to install your app</code> and how to run your app.</p>
<h3>How can I access my docode server from the browser?</h3>
<p>1 -- Open your server
Make your server <code>listening</code> on 0.0.0.0
And make sure the listening port is <code>8080</code></p>
<p>2 -- Your server will be accessible at this URL:
XXXXXXXXX is your docode ID
http://web-XXXXXXXXX.docode.YYYY.qwasar.io</p>
<p>Example:</p>
<pre class=" language-plain"><code class=" language-plain">If your docode url is:
abc123.docode.us.qwasar.io
then your url will be:
http://abc123.docode.us.qwasar.io
</code></pre>
<img src="https://storage.googleapis.com/qwasar-public/track-web/docode-ide-web.png" width="500px">
<p><strong>Tips</strong>
Google Flask
Google HTTP Code (200, 204, 400, 401, 500)
Google HTTP Basic access authentication
Google curl (-i, -I, -X GET, etc)</p>

<p></p>
</div>

</div>
</div>
</div>
<div class="tab-pane" id="resources" role="tabpanel">
<div class="row">
<div class="col-xl-12">
<div class="row text-center">
<div class="col p-t-10 f-12">
<p>
Python Flask Tutorial: Full-Featured Web App
</p>
</div>
</div>
<div class="row text-center">
<div class="col">
<iframe frameborder="0" src="https://www.youtube.com/embed/MwZwr5Tvyxo"></iframe>
</div>
</div>
<hr>
<div class="row text-center">
<div class="col p-t-10 f-12">
<p>
My IMDB Api - Create a webserver
</p>
</div>
</div>
<div class="row text-center">
<div class="col">
<iframe frameborder="0" src="https://www.youtube.com/embed/ZuPO7NegBb4"></iframe>
</div>
</div>
<hr>
<div class="row text-center">
<div class="col p-t-10 f-12">
<p>
My IMDB Api - Filter a CSV
</p>
</div>
</div>
<div class="row text-center">
<div class="col">
<iframe frameborder="0" src="https://www.youtube.com/embed/CC9yl9Bg0oc"></iframe>
</div>
</div>
<hr>
<div class="row text-center">
<div class="col p-t-10 f-12">
<p>
My IMDB Api - Receive Params and return JSON
</p>
</div>
</div>
<div class="row text-center">
<div class="col">
<iframe frameborder="0" src="https://www.youtube.com/embed/6y2JelXq-1E"></iframe>
</div>
</div>
<hr>
<div class="row text-center">
<div class="col p-t-10 f-12">
<p>
How To Create a Group
</p>
</div>
</div>
<div class="row text-center">
<div class="col">
<iframe frameborder="0" src="https://www.youtube.com/embed/g5WyMfFdHc4"></iframe>
</div>
</div>
<hr>
<div class="row text-center">
<div class="col p-t-10 f-12">
<p>
How To Do A README?
</p>
</div>
</div>
<div class="row text-center">
<div class="col">
<iframe frameborder="0" src="https://www.youtube.com/embed/uMkrJ9dw3bc"></iframe>
</div>
</div>

</div>
</div>
</div>
</div>
</div>
</div>
