Descriptive metadata attributes can be used to describe the content item to the user, in a user interface element that allows the user to select the item.

<table>
<thead>
<tr>
<th class="short-line">Attributes</th>
<th class="short-line">Type</th>
<th class="short-line">Values</th>
<th class="short-line">Example</th>
</tr>
</thead>
<tbody>
<tr>
<td class="short-line">ContentType</td>
<td class="short-line">String</td>
<td class="long-line">Although ContentType accepts type String, the return value is of type <a href="/docs/references/brightscript/components/roint.md">roInt</a>. See table below. <div class="hscroll"><table>
<thead>
<tr>
<th class="short-line">Content Type</th>
<th class="short-line">Return Value</th>
</tr>
</thead>
<tbody>
<tr>
<td class="short-line">audio</td>
<td class="short-line">5</td>
</tr>
<tr>
<td class="short-line">episode</td>
<td class="short-line">4</td>
</tr>
<tr>
<td class="short-line">movie</td>
<td class="short-line">1</td>
</tr>
<tr>
<td class="short-line">not set or not supported</td>
<td class="short-line">0</td>
</tr>
<tr>
<td class="short-line">season</td>
<td class="short-line">3</td>
</tr>
<tr>
<td class="short-line">series</td>
<td class="short-line">2</td>
</tr>
</tbody>
</table></div></td>
<td class="short-line">"movie"</td>
</tr>
<tr>
<td class="short-line">Title</td>
<td class="short-line">String</td>
<td class="long-line">Content title: movie title for films; episode title for TV series</td>
<td class="short-line">"The Dark Knight"</td>
</tr>
<tr>
<td class="short-line">TitleSeason</td>
<td class="short-line">String</td>
<td class="short-line">Season title for TV series</td>
<td class="short-line">"Battlestar Galactica Season 5"</td>
</tr>
<tr>
<td class="short-line">Description</td>
<td class="short-line">String</td>
<td class="short-line">Description of content</td>
<td class="short-line">"Batman, Gordon and Harvey Dent are forced…"</td>
</tr>
<tr>
<td class="short-line">SDPosterUrl</td>
<td class="short-line">String</td>
<td class="short-line">URL for SD content artwork</td>
<td class="long-line"><a href="http://www.myco.com/img/sd1932.jpg">http://www.myco.com/img/sd1932.jpg</a></td>
</tr>
<tr>
<td class="short-line">HDPosterUrl</td>
<td class="short-line">String</td>
<td class="short-line">URL for HD content artwork</td>
<td class="long-line"><a href="http://www.myco.com/img/hd1932.jpg">http://www.myco.com/img/hd1932.jpg</a></td>
</tr>
<tr>
<td class="short-line">FHDPosterUrl</td>
<td class="short-line">String</td>
<td class="short-line">URL for FHD content artwork</td>
<td class="long-line"><a href="http://www.myco.com/img/fhd1932.jpg">http://www.myco.com/img/fhd1932.jpg</a></td>
</tr>
<tr>
<td class="short-line">ReleaseDate</td>
<td class="short-line">String</td>
<td class="short-line">Formatted Date String</td>
<td class="short-line">"3/31/2009"</td>
</tr>
<tr>
<td class="short-line">Rating</td>
<td class="short-line">String</td>
<td class="long-line">Selects an icon to be displayed for the corresponding MPAA or TV rating, that is, the value will display as an icon artwork. See <a href="/docs/developer-program/getting-started/architecture/content-metadata.md#rating-attribute-icons">Rating Attribute Icons</a> for a list of the acceptable values and the corresponding icon.</td>
<td class="short-line">"PG-13"</td>
</tr>
<tr>
<td class="short-line">StarRating</td>
<td class="short-line">Integer</td>
<td class="long-line">Specifies the star rating to display as red star icon artwork, as a number from 1 to 100: <ul>
<li>20 displays one star</li>
<li>40 displays two stars</li>
<li>60 displays three stars</li>
<li>80 displays four stars</li>
<li>100 displays five stars</li>
</ul> Numbers not divisible by 20 are displayed as a fractional star (A number of 30 will display one and a half stars)</td>
<td class="short-line">80</td>
</tr>
<tr>
<td class="short-line">UserStarRating</td>
<td class="short-line">Integer</td>
<td class="long-line">Specifies the user star rating to display as yellow star icon artwork, as a number from 1 to 100: <ul>
<li>20 displays one star</li>
<li>40 displays two stars</li>
<li>60 displays three stars</li>
<li>80 displays four stars</li>
<li>100 displays five stars</li>
</ul> Does not display fractional stars for numbers not divisible by 20</td>
<td class="short-line">80</td>
</tr>
<tr>
<td class="short-line">ShortDescriptionLine1</td>
<td class="short-line">String</td>
<td class="short-line">Line 1 of Poster Screen Description</td>
<td class="short-line">"The Dark Knight"</td>
</tr>
<tr>
<td class="short-line">ShortDescriptionLine2</td>
<td class="short-line">String</td>
<td class="short-line">Line 2 of Poster Screen Description</td>
<td class="short-line">"Rent $1.99, Buy $14.99"</td>
</tr>
<tr>
<td class="short-line">EpisodeNumber</td>
<td class="short-line">String</td>
<td class="short-line">Episode Number</td>
<td class="short-line">"1"</td>
</tr>
<tr>
<td class="short-line">NumEpisodes</td>
<td class="short-line">Integer</td>
<td class="long-line">Number of episodes for a "season" or "series" contentType</td>
<td class="short-line">40</td>
</tr>
<tr>
<td class="short-line">Actors</td>
<td class="short-line">roArray</td>
<td class="short-line">List of Actor Names</td>
<td class="short-line">["Brad Pitt", "Angelina Jolie"]</td>
</tr>
<tr>
<td class="short-line">Actors</td>
<td class="short-line">String</td>
<td class="short-line">Individual Actor Name</td>
<td class="short-line">"Brad Pitt"</td>
</tr>
<tr>
<td class="short-line">Directors</td>
<td class="short-line">roArray</td>
<td class="short-line">List of Director Names</td>
<td class="short-line">["Joel Coen", "Clint Eastwood"]</td>
</tr>
<tr>
<td class="short-line">Director</td>
<td class="short-line">String</td>
<td class="short-line">Individual Director Name</td>
<td class="short-line">"Christopher Nolan"</td>
</tr>
<tr>
<td class="short-line">Categories</td>
<td class="short-line">roArray</td>
<td class="short-line">List of Category/Genre Names</td>
<td class="short-line">["Comedy", "Drama"]</td>
</tr>
<tr>
<td class="short-line">Categories</td>
<td class="short-line">String</td>
<td class="short-line">Individual Category/Genre Name</td>
<td class="short-line">"Comedy"</td>
</tr>
<tr>
<td class="short-line">Album</td>
<td class="short-line">String</td>
<td class="long-line">roSpringboard audio style uses this to display the album</td>
<td class="short-line">"Achtung"</td>
</tr>
<tr>
<td class="short-line">Artist</td>
<td class="short-line">String</td>
<td class="short-line">roSpringboard audio style uses to show artist</td>
<td class="short-line">"U2"</td>
</tr>
<tr>
<td class="short-line">TextOverlayUL</td>
<td class="short-line">String</td>
<td class="long-line">roSlideShow displays this string in Upper Left corner of slide</td>
<td class="short-line">"Joe's Photos"</td>
</tr>
<tr>
<td class="short-line">TextOverlayUR</td>
<td class="short-line">String</td>
<td class="long-line">roSlideShow displays this string in Upper Right corner of slide</td>
<td class="short-line">"3 of 20"</td>
</tr>
<tr>
<td class="short-line">TextOverlayBody</td>
<td class="short-line">String</td>
<td class="long-line">roSlideShow displays this string on the bottom part of slide</td>
<td class="short-line">"Wanda's 40'th Birthday"</td>
</tr>
</tbody>
</table>