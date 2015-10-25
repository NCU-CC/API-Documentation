# Get Person Information by Card Number

```
GET /cards/{card_number}
```

## Description
> Get person information by NCU card number. Read the NCU card number by devices with NFC.

## Required Scope
- user.info.basic.read

# Request

## Query Parameters
<table>
  <tr>
    <td><b>Name</b></td>
    <td><b><b>Required</b></b></td>
    <td><b>Description</b></td>
  </tr>
  <tr>
	<td><b>id</b></td>
	<td><i>yes</i></td>
	<td>the last 4 digits of your id card number (身分證字號) for security purpose</td>
  </tr>
</table>

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
GET /cards/F06D4935?id=1234
```

```
GET /cards/F06D2549?id=6789
```

# Response

## Formats
- json

## Structure
There are two types of response. You can verify the type by **type** attribute

- Student

    <table>
        <tr>
            <td><b>Field Name</b></td>
            <td><b>Type</b></td>
            <td><b>Value Description</b></td>
        </tr>
        <tr>
           <td>name</td>
           <td>String</td>
           <td>person name</td>
        </tr>
        <tr>
           <td>type</td>
           <td>String</td>
           <td>person type, this must be <strong>STUDENT</strong> here</td>
        </tr>
        <tr>
           <td>unit</td>
           <td>String</td>
           <td>student unit</td>
        </tr>
        <tr>
           <td>group</td>
           <td>String</td>
           <td>student group</td>
        </tr>
        <tr>
           <td>number</td>
           <td>String</td>
           <td>student number</td>
        </tr>
    </table>
    
- Faculty

    <table>
        <tr>
            <td><b>Field Name</b></td>
            <td><b>Type</b></td>
            <td><b>Value Description</b></td>
        </tr>
        <tr>
           <td>name</td>
           <td>String</td>
           <td>person name</td>
        </tr>
        <tr>
           <td>type</td>
           <td>String</td>
           <td>person type, this must be <strong>FACULTY</strong> here</td>
        </tr>
        <tr>
           <td>unit</td>
           <td>String</td>
           <td>faculty unit</td>
        </tr>
        <tr>
           <td>title</td>
           <td>String</td>
           <td>faculty title</td>
        </tr>
        <tr>
           <td>number</td>
           <td>String</td>
           <td>faculty number</td>
        </tr>
    </table>

## Example
```json
{
    "name" : "john",
    "type" : "STUDENT",
    "unit" : "computer science",
    "group" : "none",
    "number" : "101502549",
}
```

```json
{
    "name" : "jack",
    "type" : "FACULTY",
    "unit" : "computer center",
    "title" : "software developer",
    "number" : "F123456"",
}
```