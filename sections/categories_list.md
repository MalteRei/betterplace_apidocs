
# Project Categories List

```Cirru
GET https://api.betterplace.org/de/api_v4/projects/1114/categories.json?order=position%3AASC
```

A list of betterplace.org project categories.
Results are contained in a *data* attribute.


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
  <tr>
    <th align="left">order</th>
    <td><code>position:ASC</code></td>
    <td>no</td>
<td>

Order the result set. Documented and supported orders are:
<ul>
  <li><code>position:asc/desc</code> – Position of the category.
</ul>
<a href="../README.md#request-parameter-format">Learn how to format the parameter</a>.


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
      <th align="left">name</th>
      <td><code>string</code></td>
      <td><code></code></td>
<td>

Name to be displayed for this category

</td>
    </tr>
    <tr>
      <th align="left">slug</th>
      <td><code>string</code></td>
      <td><code></code></td>
<td>

Slug for this category

</td>
    </tr>
    <tr>
      <th align="left">position</th>
      <td><code>number</code></td>
      <td><code></code></td>
<td>

Position this category should be displayed at

</td>
    </tr>
    <tr>
      <th align="left">page_title</th>
      <td><code>string</code></td>
      <td><code></code></td>
<td>

Page title to be displayed for this category

</td>
    </tr>
    <tr>
      <th align="left">social_media_description</th>
      <td><code>string</code></td>
      <td><code></code></td>
<td>

Description to be used on social media for this category

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

platform

</th>
<td>

Permalink to betterplace.org discover category

</td>
    </tr>
</table>

## Response Example

```json
{
  "total_entries": 3,
  "offset": 0,
  "total_pages": 1,
  "current_page": 1,
  "per_page": 3,
  "data": [
    {
      "id": 3,
      "created_at": "2016-12-13T16:18:14+01:00",
      "updated_at": "2018-12-03T17:26:13+01:00",
      "name": "Bildung",
      "slug": "bildung",
      "position": 3,
      "page_title": "Spende für Bildung auf betterplace.org",
      "social_media_description": "Entdecke Bildungsprojekte auf betterplace.org und spende Kindern nicht nur Bildung, sondern Zukunft!",
      "links": [
        {
          "rel": "platform",
          "href": "https://www.betterplace.org/de/discover-projects/3-bildung"
        }
      ]
    },
    {
      "id": 15,
      "created_at": "2016-12-13T17:07:22+01:00",
      "updated_at": "2018-03-02T12:21:51+01:00",
      "name": "Sport",
      "slug": "sport",
      "position": 1000,
      "page_title": "Spenden für Sportprojekte auf betterplace.org",
      "social_media_description": "Finde spannende Projekte zum Thema Sport",
      "links": [
        {
          "rel": "platform",
          "href": "https://www.betterplace.org/de/discover-projects/15-sport"
        }
      ]
    },
    {
      "id": 2,
      "created_at": "2016-12-13T16:17:58+01:00",
      "updated_at": "2019-08-23T15:43:38+02:00",
      "name": "Kinder und Jugend",
      "slug": "kinder",
      "position": 3,
      "page_title": "Spenden für Kinder auf betterplace.org",
      "social_media_description": "Entdecke großartige Projekte, die sich für Kinder und Jugendliche weltweit einsetzen, und sorge mit deiner Spende glückliche Kinderaugen!",
      "links": [
        {
          "rel": "platform",
          "href": "https://www.betterplace.org/de/discover-projects/2-kinder"
        }
      ]
    }
  ]
}
```

