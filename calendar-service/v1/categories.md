# Get Categories

```
GET /categories
```

## Description
> Return categories.

# Request

## Headers
<table>
  <tr>
    <td><b>Name</b></td>
    <td><b>Required</b></td>
    <td><b>Description</b></td>
  </tr>
  <tr>
    <td><b>Authorization</b></td>
    <td><i>yes</i></td>
    <td>Bearer token</td>
  </tr>
</table>

## Example

```
GET /categories
```

# Response

## Formats
- json

## Structure
<table>
   <tr>
      <td><b>Field Name</b></td>
      <td><b>Type</b></td>
      <td><b>Value Description</b></td>
   </tr>
   <tr>
      <td>categories</td>
      <td>array</td>
      <td>A list of Category.</td>
   </tr>
</table>

### Category
<table>
   <tr>
      <td><b>Field Name</b></td>
      <td><b>Type</b></td>
      <td><b>Value Description</b></td>
   </tr>
   <tr>
      <td>id</td>
      <td>integer</td>
      <td>Category identifier.</td>
   </tr>
   <tr>
      <td>name</td>
      <td>string</td>
      <td>Name of category.</td>
   </tr>
   <tr>
      <td>calendar_id</td>
      <td>string</td>
      <td>Calendar identifier of Google Calendar.</td>
   </tr>
   <tr>
      <td>addible</td>
      <td>boolean</td>
      <td>Whether this category is addible.</td>
   </tr>
</table>

## Example
```json
{
  "categories": [
    {
      "id": 1,
      "name": "校曆",
      "calendar_id": "vul4xu4@group.calendar.google.com",
      "addible": false
    },
    {
      "id": 2,
      "name": "教職員",
      "calendar_id": "rul456m06@group.calendar.google.com",
      "addible": true
    },
    {
      "id": 3,
      "name": "學生",
      "calendar_id": "vm6g@group.calendar.google.com",
      "addible": true
    }
  ]
}
```
