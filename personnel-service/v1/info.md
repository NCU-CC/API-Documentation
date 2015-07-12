# Get Person Information

```
GET /info
```

## Description
> Get person information from access token

## Required Scope
- user.info.basic.read

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
        <td>Your OAuth token in the form of <code>Bearer XXX</code></td>
    </tr>
</table>

## Example
```
GET /info
```

# Response

## Formats
- json

## Structure
[Person Object](cards.md#structure)

## Example
[Person Example](cards.md#example-1)