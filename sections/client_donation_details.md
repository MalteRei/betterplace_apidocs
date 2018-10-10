
# Client Donation Details ⇄ [List](client_donations_list.md)

```Cirru
GET https://api.betterplace.org/de/api_v4/clients/volksfreund/client_donations/aacf667a485010b23c0f.json
```

**For [betterplace.org clients](../README.md#client-api) only:**

The details of a betterplace.org client donation.
The details and list view show the same data.


## URL Parameters

<table>
  <tr>
    <th>Parameter</th>
    <th>Example</th>
    <th>Required</th>
    <th>Description</th>
  </tr>
  <tr>
    <th align="left">client_id</th>
    <td><code>volksfreund</code></td>
    <td>yes</td>
<td>

The betterplace.org-internal client permalink.

</td>
  </tr>
  <tr>
    <th align="left">id</th>
    <td><code>aacf667a485010b23c0f</code></td>
    <td>yes</td>
<td>

          The donation token that the client donation form passed to the
          callback url or the client_reference that was provided by the client.


</td>
  </tr>
</table>


## Response Attributes

  <th colspan="4">No response example defined</th>
</table>

## Response Links

<table>
  <tr>
    <th>Linkname</th>
    <th>Description</th>
  </tr>
  <th colspan="2">No response example defined</th>
</table>

## Response Example

```json
[
  "/Users/flori/scm/betterplace/app/controllers/api_v4/client_donations_controller.rb:98:in `block (2 levels) in <class:ClientDonationsController>'"
]
```

