
# Project Blog Posts List ⇄ [Details](blog_post_details.md)

```Cirru
GET https://api.betterplace.org/de/api_v4/projects/1114/blog_posts.json
```

A list of the blog posts of a betterplace.org project.
Results are contained in a *data* attribute.

**For [betterplace.org clients](../README.md#client-api):**

* _Project Blogposts:_ There is no client-scoped URL.
Please use the API calls that are provided inside the client project _url_ response
to make sure you only request data that is associated with one of your projects.

* _All Blogposts:_ Clients can retrieve a list of all blogpost of all client projects:
`/clients/PERMALINK/blog_posts.json`


## URL Parameters

<table>
  <tr>
    <th>Parameter</th>
    <th>Example</th>
    <th>Required</th>
    <th>Description</th>
  </tr>
  <tr>
    <th align="left">project_id</th>
    <td><code>1114</code></td>
    <td>yes</td>
<td>

Project id as an integer number ≥ 14.

</td>
  </tr>
</table>


## Response Attributes


### Root Attributes

  <table>
    <tr>
      <th>Attribute</th>
      <th>Types</th>
      <th>Example</th>
      <th>Description</th>
    </tr>
    <tr>
      <th align="left">id</th>
      <td><code>number</code></td>
      <td><code>1</code></td>
<td>

An integer number ≥ 1

</td>
    </tr>
    <tr>
      <th align="left">created_at</th>
      <td><code>string</code></td>
      <td><code>"1994-11-05T13:15:30Z"</code></td>
<td>

DateTime (ISO8601 with Timezone)

</td>
    </tr>
    <tr>
      <th align="left">updated_at</th>
      <td><code>string</code></td>
      <td><code>"1994-11-05T13:15:30Z"</code></td>
<td>

DateTime (ISO8601 with Timezone)

</td>
    </tr>
    <tr>
      <th align="left">lang</th>
      <td><code>string</code></td>
      <td><code>en</code></td>
<td>

Blog posts have only one language at the moment

</td>
    </tr>
    <tr>
      <th align="left">type</th>
      <td><code>string</code></td>
      <td><code>BlogPost</code></td>
<td>

Blogposts are always created by a user, and this
field always has the value <code>BlogPost</code>.


</td>
    </tr>
    <tr>
      <th align="left">title</th>
      <td><code>string</code></td>
      <td><code>Thank you from Beijing</code></td>
<td>



</td>
    </tr>
    <tr>
      <th align="left">body</th>
      <td><code>string</code></td>
      <td><code>I am so happy to hear about the first donation for the Good Gifted Garden. If I told Chun …</code></td>
<td>

The body may contain html such as links, embedded videos, and picture or
any of the following HTML tags:
```a, b, br, div, em, i, iframe, img, li, ol, p, strong, ul```.


</td>
    </tr>
    <tr>
        <th align="left" style="white-space: nowrap">
          <a id="author-ref" href="#author">
            ↓author
          </a>
        </th>
      <td><code>string</code></td>
      <td><code>"Till B."</code></td>
<td>

Display name of a betterplace.org user.
Possible formats: "Till B.", "T. Behnke", "Till Behnke"


</td>
    </tr>
  </table>

### <a id="author" href="#author-ref">↑Nested Attributes: author</a>

  <table>
    <tr>
      <th>Attribute</th>
      <th>Types</th>
      <th>Example</th>
      <th>Description</th>
    </tr>
    <tr>
      <th align="left">author.id</th>
      <td><code>number</code></td>
      <td><code>1</code></td>
<td>

An integer number ≥ 1

</td>
    </tr>
    <tr>
      <th align="left">author.name</th>
      <td><code>null &#124; string</code></td>
      <td><code>"Till B."</code></td>
<td>

Display name of a betterplace.org user.
Possible formats: "Till B.", "T. Behnke", "Till Behnke".

In the case of donation-opinions the name might also be
empty/null for anonymous donations for anonymous donations.


</td>
    </tr>
    <tr>
        <th align="left" style="white-space: nowrap">
          <a id="author.picture-ref" href="#author.picture">
            ↓author.picture
          </a>
        </th>
      <td><code>object</code></td>
      <td><code>//betterplace-assets.betterplace.org ↪/uploads/user/profile_picture ↪/000/000/001 ↪/fill_100x100_original_tb.jpg</code></td>
<td>

User profile picture or a fallback image

</td>
    </tr>
  </table>

### <a id="author.picture" href="#author.picture-ref">↑Nested Attributes: author.picture</a>

  <table>
    <tr>
      <th>Attribute</th>
      <th>Types</th>
      <th>Example</th>
      <th>Description</th>
    </tr>
    <tr>
      <th align="left">author.picture.fallback</th>
      <td><code>boolean</code></td>
      <td><code>true</code></td>
<td>

Specifies whether a fallback image is given or not

</td>
    </tr>
  </table>
</table>

## Response Links

<table>
  <tr>
    <th>Linkname</th>
    <th>Description</th>
  </tr>
    <tr>
<th align="left">

self

</th>
<td>

Link to this resource itself
(<a href="blog_post_details.md">blog post details</a>)


</td>
    </tr>
    <tr>
<th align="left">

platform

</th>
<td>

Permalink to betterplace.org

</td>
    </tr>
    <tr>
<th align="left">

documentation

</th>
<td>

Link to this resource in the documentation


</td>
    </tr>
    <tr>
<th align="left">

author.platform

</th>
<td>

The user's profile on betterplace.org.
To view a user profile you have to be logged in.
This array is empty if the user has no useraccount
with betterplace.org but donated via one of our partner.


</td>
    </tr>
    <tr>
<th align="left">

author.contact_data

</th>
<td>

The user's contact data. Please note that you need to be
<a href="../README.md#client-api">authenticated as a client</a> with matching
access rights in order to see this information.


</td>
    </tr>
    <tr>
<th align="left">

author.picture.fill_100x100

</th>
<td>

100×100 Pixel

</td>
    </tr>
    <tr>
<th align="left">

author.picture.original

</th>
<td>

Maximum sized image. This is the original image with default-cropping or user-cropping applied.

</td>
    </tr>
</table>

## Response Example

```json
{
  "total_entries": 94,
  "offset": 0,
  "total_pages": 47,
  "current_page": 1,
  "per_page": 2,
  "data": [
    {
      "id": 111316,
      "created_at": "2015-03-05T14:38:47+01:00",
      "updated_at": "2017-07-11T09:27:31+02:00",
      "lang": "de",
      "type": "BlogPost",
      "title": "The Future of Afghanistan",
      "body": "<p></p><br><p>What does the future hold for us? How do we make it brighter?</p><br><br><p>Growing up in a war torn community is tough, but Afghan youth at Skateistan are learning to build better futures for themselves.</p><br><p><img src=\"https://asset1.betterplace.org/uploads/project/image/000/001/114/101548/limit_600x450_image.jpg\" alt=\"Limit 600x450 image\"><br></p><br><br><p>In the city of Kabul at Skateistan's very first skate school, <br>students have just completed the 'Future' education curriculum. <br>Students worked on their own personal “time-clocks\", set life goals and <br>learnt all about how to achieve their dreams. Amazing inventions for the<br> future were made from all sorts of material to benefit the community - <br>including an electronic skateboard, water filters and a DIY hot air <br>balloon to beat traffic! At <strong><a href=\"http://skateistan.org/blog/5th-anniversary-skateistan-kabul\">Skateistan’s 5th Anniversary</a></strong><br> event we even held a student invention competition that was judged by <br>Ambassador Henk Jan Bakker, from the Embassy of the Netherlands in <br>Kabul. The Ambassador gave Skateistan students 1 hour to create a <br>solution to a problem in the city. He asked them, \"How can people have clean water in Kabul?\" The girls team won the trophy for the best invention that day for creating a very detailed water purification plant.</p><br><br><p>We also invited famous community members to talk to the students <br>about their careers and offer advice on how to contribute to rebuilding <br>the country. Skateistan’s very first time capsule was created with <br>messages from current students to Skateistan students of the future. <br>Students even got to explore what it would be like to be Mayor of the <br>city for a day, and decide what they would do with such responsibility. <br>With inventions, field trips, LEGO and other interactive learning <br>activities, this curriculum was one of Skateistan’s most successful, and<br> a student favorite. It encouraged children to consider the importance <br>of their connection with the future and the past, how things change over<br> time and most importantly, how to plan and prioritize goals for their <br>own lives. </p><br><br><br><p><em>\"My favorite lesson was self-confidence because if we learn a lot<br> about this short word we will improve very much in our life, because to<br> trust yourself is victory. Once we say we can do everything then we can<br> put it into action.”</em><br><br>- Basina, Student, 13 years old</p><br><br><br><br><p><em>“One of my favorite semesters at Skateistan was the future <br>semester. I learnt a lot of things like how to organize my life goals <br>and to achieve my career goals. It gave me ideas on how to invent good <br>ways of life and grow more in life.”</em><br><br>- Tamana, Student, 11 years old</p><br><p></p><br><p><img src=\"https://asset1.betterplace.org/uploads/project/image/000/001/114/101546/limit_600x450_image.jpg\" alt=\"Limit 600x450 image\"><br></p><br><p><em>“Our class invented a water-cleaning model, which we can use in <br>dirty water. It’s something like a pipe and once we put it in a teapot <br>it acts like a filter and cleans the water.”</em><br><br>- Basina, Student, 13 years old<br></p><br><p>We asked some Skateistan students about what their plans are for the future: </p><br><br><br><p><em>“I would like to become a pilot <br>and serve my people and my message for others is to study hard and <br>achieve their life goals and the only way to receive your dreams is by <br>studying hard.”</em><br><br>- Babor Shah, Student, 12 years old</p><br><br><p><em>“I want to be a journalist and give the rights of all people by <br>broadcasting the truth. My message for others is that you are the best -<br> just have confidence in yourself.”</em><br><br>- Hasibullah, Student, 17 years old</p><br><br><p><em>“I want to become a doctor and rescue all my people. Some people <br>are always going outside of the country and spending a bunch of money <br>but if I become a doctor I will make a special discount for people and <br>it will help all of the people in Afghanistan to rescue their lives and <br>the money that is going outside of the country.\"</em><br><br>- Hedayatullah, Student, 13 years old</p><br><br><p><em>“I would like to be an engineer in the future and want to help rebuild my country.”</em><br><br>- Ahmad Sorosh, Student 12 years old</p><br><br><p><em>“I want to be a skate teacher and my message is to study hard and play sport.”</em><br><br>- Zaker, Student, 13 years old</p><br><p>We asked some Skateistan students about what their plans are for the future: </p><br><br><br><p><em>“I would like to become a pilot <br>and serve my people and my message for others is to study hard and <br>achieve their life goals and the only way to receive your dreams is by <br>studying hard.”</em><br><br>- Babor Shah, Student, 12 years old</p><br><br><p><em>“I want to be a journalist and give the rights of all people by <br>broadcasting the truth. My message for others is that you are the best -<br> just have confidence in yourself.”</em><br><br>- Hasibullah, Student, 17 years old</p><br><br><p><em>“I want to become a doctor and rescue all my people. Some people <br>are always going outside of the country and spending a bunch of money <br>but if I become a doctor I will make a special discount for people and <br>it will help all of the people in Afghanistan to rescue their lives and <br>the money that is going outside of the country.\"</em><br><br>- Hedayatullah, Student, 13 years old</p><br><br><p><em>“I would like to be an engineer in the future and want to help rebuild my country.”</em><br><br>- Ahmad Sorosh, Student 12 years old</p><br><br><p><em>“I want to be a skate teacher and my message is to study hard and play sport.”</em><br><br>- Zaker, Student, 13 years old</p><br><p><img src=\"https://asset1.betterplace.org/uploads/project/image/000/001/114/101549/limit_600x450_image.jpg\" alt=\"Limit 600x450 image\"><br></p><br><p>For many children in Afghanistan, the future holds little hope. Often it<br> is the endless repetition of selling chewing gum in the streets or <br>washing cars in the harsh Afghan winter to provide for the family. At <br>Skateistan, students have the opportunity to change, to make their own <br>futures brighter.<br></p><br><p></p>",
      "author": null,
      "links": [
        {
          "rel": "self",
          "href": "https://api.betterplace.org/de/api_v4/blog_posts/111316.json"
        },
        {
          "rel": "platform",
          "href": "https://www.betterplace.org/de/projects/1114-skateistan-afghanistan/news/111316"
        },
        {
          "rel": "documentation",
          "href": "https://github.com/betterplace/betterplace_apidocs/blob/master/sections/blog_post_details.md"
        }
      ]
    },
    {
      "id": 95557,
      "created_at": "2014-03-31T17:16:38+02:00",
      "updated_at": "2017-03-17T13:10:07+01:00",
      "lang": "de",
      "type": "BlogPost",
      "title": "Für diese Bedarfe habe ich eine (Teil-)Auszahlung veranlasst:",
      "body": "<p>A big thank you to everyone who has donated to Skateistan!</p><br><p>All donations to Skateistan are very gratefully received and are used<br> to further our work at our projects sites. We currently have projects <br>in Afghanistan and Cambodia, with plans to expand sustainably. For more <br>information about Skateistan, or to see more ways in which your donation<br> is put to good use, please visit: <a href=\"http://www.skateistan.org\"></a><a href=\"http://www.skateistan.org\">http://www.skateistan.org</a></p><br><br><p><strong>Es wurden 805,60 € Spendengelder für folgende Bedarfe beantragt:</strong></p><ul>\n<li>Clean Water for the Skateparks in Kabul and MeS 65,60 €</li>\n<li>Kabul Skatepark Food 740,00 €</li>\n</ul>",
      "author": null,
      "links": [
        {
          "rel": "self",
          "href": "https://api.betterplace.org/de/api_v4/blog_posts/95557.json"
        },
        {
          "rel": "platform",
          "href": "https://www.betterplace.org/de/projects/1114-skateistan-afghanistan/news/95557"
        },
        {
          "rel": "documentation",
          "href": "https://github.com/betterplace/betterplace_apidocs/blob/master/sections/blog_post_details.md"
        }
      ]
    }
  ]
}
```

