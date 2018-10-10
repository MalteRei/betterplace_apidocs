
# Illustrations List

```Cirru
GET https://api.betterplace.org/de/api_v4/illustrations.json?facets=project_id%3A1114&order=amount_in_cents%3Adesc
```

A list of betterplace.org project illustrations.
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
    <th align="left">facets</th>
    <td><code>project_id:1114</code></td>
    <td>no</td>
<td>

Filter the result set.
<br>
It is strongly recommended to <strong>specify facets</strong> with each request.
A recommended set of facets is <code>tax_deductible:true| completed:false|
closed:false| prohibit_donations:false</code> (without the spaces) which
only shows active projects that can receive donations.
<br>
<em>Supported filters are:</em>
<ul>
<li><code>project_id:1114/false</code>
</ul>
It is possible to set multiple facet filters.
<a href="../README.md#request-parameter-format">Learn how to format the parameter</a>.


</td>
  </tr>
  <tr>
    <th align="left">order</th>
    <td><code>amount_in_cents:desc</code></td>
    <td>no</td>
<td>

Order the result set.
<br>
It is strongly recommended to <strong>specify an order</strong> with each request.
The default order might change at any time without notice.
<br>
<em>Supported orders are:</em>
<ul>
<li><code>amount_in_cents:asc/desc</code></li>
<li><code>project_id:asc/desc</code></li>
<li><code>created_at:asc/desc</code> and <code>updated_at:ASC/DESC</code>
<li><code>id:asc/desc</code>
</ul>
It is possible to set multiple order parameters.
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
      <th align="left">amount_in_cents</th>
      <td><code>number</code></td>
      <td><code>666</code></td>
<td>

Suggested amount to donate in cents

</td>
    </tr>
    <tr>
      <th align="left">title</th>
      <td><code>string</code></td>
      <td><code>Little cheetah kittens need your help</code></td>
<td>

Title of the illustration

</td>
    </tr>
    <tr>
      <th align="left">description</th>
      <td><code>string</code></td>
      <td><code>They really do…</code></td>
<td>

More detailed description of the illustration

</td>
    </tr>
    <tr>
        <th align="left" style="white-space: nowrap">
          <a id="picture-ref" href="#picture">
            ↓picture
          </a>
        </th>
      <td><code>null &#124; object</code></td>
      <td><code>See below</code></td>
<td>

Picture to be displayed in the illustration

</td>
    </tr>
  </table>

### <a id="picture" href="#picture-ref">↑Nested Attributes: picture</a>

  <table>
    <tr>
      <th>Attribute</th>
      <th>Types</th>
      <th>Example</th>
      <th>Description</th>
    </tr>
    <tr>
      <th align="left">picture.fallback</th>
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

new_donation

</th>
<td>

Link to where a new donation can be made

</td>
    </tr>
    <tr>
<th align="left">

project

</th>
<td>

Link to the project this illustration belongs to
(<a href="project_details.md">project details</a>)


</td>
    </tr>
    <tr>
<th align="left">

picture.fill_410x214

</th>
<td>

Illustration picturw with 410×214 Pixel

</td>
    </tr>
</table>

## Response Example

```json
{
  "total_entries": 62,
  "offset": 0,
  "total_pages": 21,
  "current_page": 1,
  "per_page": 3,
  "data": [
    {
      "id": 1,
      "created_at": "2018-08-28T13:49:16+02:00",
      "updated_at": "2018-08-28T13:52:55+02:00",
      "amount_in_cents": 2000,
      "title": "Nahrung",
      "description": "Bereits mit BETRAG können wir ein Kind in Syrien einen Monat lang mit Nahrung unterstützen.",
      "picture": {
        "links": [
          {
            "rel": "fill_410x214",
            "href": "https://betterplace-assets.betterplace.org/uploads/illustration/picture/000/000/001/fill_410x214_bp1535457175_Syrien-nothilfe-kinder-familien_007_171103_.jpg"
          }
        ]
      },
      "links": [
        {
          "rel": "new_donation",
          "href": "https://api.betterplace.org/de/projects/10377-syrien-hilfe-fur-kinder/donations/new?donation_amount=20"
        },
        {
          "rel": "project",
          "href": "https://api.betterplace.org/de/api_v4/projects/10377.json"
        }
      ]
    },
    {
      "id": 2,
      "created_at": "2018-08-28T13:55:58+02:00",
      "updated_at": "2018-08-28T13:56:35+02:00",
      "amount_in_cents": 10000,
      "title": "Wasser-Pumpen",
      "description": "Bereits mit BETRAG können wir mehrere Familien mit Trinkwasser versorgen und verbessern die hygienischen Bedingungen  entscheidend. ",
      "picture": {
        "links": [
          {
            "rel": "fill_410x214",
            "href": "https://betterplace-assets.betterplace.org/uploads/illustration/picture/000/000/002/fill_410x214_bp1535457395_Syrien-nothilfe-verteilung-kinder_002_171112.jpg"
          }
        ]
      },
      "links": [
        {
          "rel": "new_donation",
          "href": "https://api.betterplace.org/de/projects/10377-syrien-hilfe-fur-kinder/donations/new?donation_amount=100"
        },
        {
          "rel": "project",
          "href": "https://api.betterplace.org/de/api_v4/projects/10377.json"
        }
      ]
    },
    {
      "id": 3,
      "created_at": "2018-08-29T10:18:08+02:00",
      "updated_at": "2018-08-29T10:21:07+02:00",
      "amount_in_cents": 6200,
      "title": "Spezialnahrung für ein schwer unterernährtes Kind",
      "description": "Mit BETRAG kann ein schwer unterernährtes Kleinkind sechs Wochen lang mit therapeutischer Spezialnahrung versorgt werden.",
      "picture": {
        "links": [
          {
            "rel": "fill_410x214",
            "href": "https://betterplace-assets.betterplace.org/uploads/illustration/picture/000/000/003/fill_410x214_bp1535530867_Spezialnahrung2_betterplace.jpg"
          }
        ]
      },
      "links": [
        {
          "rel": "new_donation",
          "href": "https://api.betterplace.org/de/projects/57620-medizinische-nothilfe-im-jemen/donations/new?donation_amount=62"
        },
        {
          "rel": "project",
          "href": "https://api.betterplace.org/de/api_v4/projects/57620.json"
        }
      ]
    }
  ]
}
```

