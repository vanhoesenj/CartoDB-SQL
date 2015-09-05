# **Resources For Using PostGIS & SQL in CartoDB**

The purpose of this resource is provide a summary of resources that explore the power of using SQL queries within CartoDB. The CartoDB platform is often seen as an easy entry option for creating interactive and visually compelling web-based maps. While true, the real power of CartoDB (IMO) lies in providing cloud-based access to PostgreSQL+PostGIS; the underlying spatially-enabled database. My assumption is that if you're reading this you probably have *some* understand of the SQL language and/or PostGIS but just want to explore how to utilize it within a browser or using JavaScript. 

# **Getting Started With PostGIS**

The best ''starting out' reference I used was "[PostGIS in Action](https://www.manning.com/books/postgis-in-action-second-edition)" by Obe and Hsu. However these are few other resources on my radar:

* This DZone [Reference Card #190](https://dzone.com/refcardz/essential-postgis) serves as a nice quick reference. You can download the PDF and tape it on your desk! Or not... 
* [Boundless](http://workshops.boundlessgeo.com/postgis-intro/) offers a nice tutorial complete with data. ***Note**: the advantage of using CartoDB is you don't need to install PostgreSQL & PostGIS on your own machine.*
* For more advanced PostGIS users I highly recommend the"[PostGIS Cookbook](http://j-vh.me/1OlPWZE)" by Corti et al. (2014). And I would follow [Steven Mather](https://twitter.com/smathermather) (for more than just PostGIS-related topics, you like drones too right?)
* I also recently ordered "[How Do I Do That In PostGIS](http://j-vh.me/1OlPI4O): Illustrating Classic GIS Tasks" by Arthur Lembo. Still need to work through this one.
* There is also "[PostGIS Essentials](http://j-vh.me/1OlQqzc)" by Angel Marquz, which I haven't reviewed or ordered.
* And lastly, if you REALLY want to dive deep into database architecture (it gets deep fast, but still fascinating), Reynold Xin maintains a great GitHub repository of [seminal papers](https://github.com/rxin/db-readings).

But is worth taking the time to develop some fluency with SQL & understand how PostGIS is different than [other](http://www.spatiallyadjusted.com/spatialtau-v2-9-geodatabase-vs-geodatabase/) spatial databases you make be more familiar with or be ready to endure some growing pains.


<p align="center">
  <img src="http://imgs.xkcd.com/comics/exploits_of_a_mom.png"> 
</p>
<p align="center">
    Source: <a href="https://xkcd.com/327/">XKCD</a>  
</p>

> "The most important motivation for the research work that resulted in the relational model was the objective of providing a sharp and clear boundary between the logical and physical aspects of database management." -- **E.F. Codd** <br><br>

---
# **Yeah Yeah, But What Can I Do With CartoDB?**
<p align="center">
  <img src="http://i.giphy.com/cg42AhGl8Ewk8.gif">
</p>
<p align="center">
    Source: <a href="http://giphy.com/gifs/reactiongifs-30-rock-bored-cg42AhGl8Ewk8">Giphy</a>
</p>

If you're not wowed by the intricacies of spatial databases, this may be the section you were looking for... The following links provide insight how to leverage the power of PostGIS specifically within CartoDB. They are organized in order of technical difficulty (although towards the end that becomes little more subjective).

* This [CartoDB](http://academy.cartodb.com/courses/04-sql-postgis.html) tutorial offers a gentle introduction to PostGIS & SQL within the browser.
* And an additional [tutorial](http://academy.cartodb.com/courses/03-cartodbjs-ground-up.html) on querying a CartoDB table using the CartoDB.js library.
* And this [video tutorial](https://www.youtube.com/watch?v=mPnuBG6wcAA) from [Eric Brelsford](https://twitter.com/ebrelsford) provides a nice visual of how basic and intermediate SQL is used within the CartoDB interface.
* This [slideshow](http://j-vh.me/1Om7qoQ) from [Guido Stein](https://twitter.com/guidos) covers the basics through calculating buffers.
* Similarly [Chris Whong](https://twitter.com/chris_whong) shows us that we can do [geoprocessing](http://blog.cartodb.com/geoprocessing-in-postgis/) in the cloud QUICKLY... You feel me right?
* [Andy Eschbacher](https://twitter.com/mrephysics) maintains the most extensive CartoDB [repository](http://cartodb.github.io/training/advanced/cartodbjs-deep-dive.html) I'm aware of and ranges from introductory to advanced.
* [Andrew Hill](https://github.com/andrewxhill/cartodb-examples) is the person who really turned me onto CartoDB and has provided insight into the power of this platform. And he's SQL crazy as [this](https://gist.github.com/andrewxhill/3875882) example demonstrates ([Javi Santana](https://twitter.com/javisantana) called him out first, [although](https://gist.github.com/javisantana) that's really just a pot calling a kettle names...).

****
## **Some Personal Favorites**

* [This](http://blog.cartodb.com/read-and-write-to-cartodb-with-the-leaflet-draw-plugin/) tutorial illustrates how to allow read/write access to one of your CartoDB tables (not just temporary queries). Moreover you get to see how capable the SQL parser within CartoDB Editor is with complex queries and how you can treat like a traditional desktop PostGIS installation.
* [This](http://blog.cartodb.com/data-sync-ogr/) recent post from [Paul Ramsey](https://twitter.com/pwramsey) demonstrates the integration of GDAL and CartoDB. He knows a thing or two about PostGIS; this is is equivalent to Paul sneezing SQL... just wait until he unveils support for querying LiDAR in CartoDB.
*  These three brief tutorials link the underlying spatial theory of the - Egenhofer inspired - DE-9IM model with practical examples of stringing together multiple SQL statements. ([Theory](http://bbvaopen4u.com/en/actualidad/introduction-geospatial-sql), [Basic](http://bbvaopen4u.com/en/actualidad/examples-geospatial-sql-i), [Advanced](http://bbvaopen4u.com/en/actualidad/examples-geospatial-sql-ii)).
*  [This](http://lifewatch.inbo.be/blog/posts/cartodb-tracking-data-tutorial.html) post from [Peter Desmet](https://twitter.com/peterdesmet) nicely highlights both the power of CartoDB and flexibility of CartoCSS. I'd encourage beginners to really explore the SQL code he shares in this post.
*  [This](http://duspviz.mit.edu/web-map-workshop/databases-leaflet-cartodb/) tutorial from [Mike Foster](https://twitter.com/mjfoster83) is probably one of the most thorough I've seen and was influenced by [Nick Martinelli's](https://twitter.com/nichom) '[Neighborhood Mapping Project](http://pnwmaps.com/neighborhoods/)' - another awesome interface. His bridges are cool too though...
*  Another SQL ninja (or maybe samurai is more alliteratively appropriate) is [Bill Morris](https://twitter.com/vtcraghead) who decided to create an [open-data portal](http://wboykinm.github.io/modular-geoportal/#15/44.4795/-73.2070) served through CartoDB. What makes this so awesome is PostGIS does the format conversations server side. 
*  And [this](http://sandbox.azavea.com/cartodbvisualization/) visual from John Branigan is still one of my favorite created using the CartoDB SQL API. You can explore the underlying code [here](http://sandbox.azavea.com/cartodbvisualization/js/functions.js).

I'm ultimately interested in how we can simplify access to the power of PostGIS by tricking folks into using new tools within the all familiar browser. I specifically want to move explorations of geologic data out Excel and traditional GIS tables into a PostGIS environment - enter, CartoDB.



<p align="center">
  <img src="https://raw.githubusercontent.com/vanhoesenj/CartoDB-SQL/master/utopia.png">
    Source: <a href="http://j-vh.me/1fy5vkt">JVH</a>
</p>
