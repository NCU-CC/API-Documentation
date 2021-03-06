# Find Course Information

```
GET /courses/{serialNo}
```

## Description
> Find course information by its id.

# Request
## Headers
<table>
  <tr>
    <td><b>Name</b></td>
    <td><b>Required</b></td>
    <td><b>Description</b></td>
  </tr>
  <tr>
    <td><b>X-NCU-API-TOKEN</b></td>
    <td><i>yes</i></td>
    <td>Your API token</td>
  </tr>
</table>

## Example
```
GET /courses/12034
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
        <td>serialNo</td>
        <td>String</td>
        <td>course id, 5 digits and left padding 0.</td>
    </tr>
    <tr>
        <td>no</td>
        <td>String</td>
        <td>course number</td>
    </tr>
    <tr>
        <td>classNo</td>
        <td>String</td>
        <td>class number, * means not specify.</td>
    </tr>
    <tr>
        <td>name</td>
        <td>String</td>
        <td>course name</td>
    </tr>
    <tr>
        <td>isClosed</td>
        <td>Boolean</td>
        <td>is canceled or not.</td>
    </tr>
    <tr>
        <td>memo</td>
        <td>String</td>
        <td>memo</td>
    </tr>
    <tr>
        <td>isMasterDoctor</td>
        <td>Boolean</td>
        <td>is both for master and doctor.</td>
    </tr>
    <tr>
        <td>language</td>
        <td>Enum</td>
        <td>language that instructor(s) use.
            <table>
                <tr>
                    <td>Chinese</td>
                    <td>中文</td>
                </tr>
                <tr>
                    <td>English</td>
                    <td>英語</td>
                </tr>
                <tr>
                    <td>French</td>
                    <td>法語</td>
                </tr>
                <tr>
                    <td>Taiwanese</td>
                    <td>台語</td>
                </tr>
                <tr>
                    <td>Hakka</td>
                    <td>客語</td>
                </tr>
                <tr>
                    <td>Japanese</td>
                    <td>日本語</td>
                </tr>
                <tr>
                    <td>Spanish</td>
                    <td>西班牙語</td>
                </tr>
                <tr>
                    <td>German</td>
                    <td>德語</td>
                </tr>
                <tr>
                    <td>Partially English</td>
                    <td>部份英語</td>
                </tr>
            </table>
        </td>
    </tr>
    <tr>
        <td>passwordCard</td>
        <td>Enum</td>
        <td>
            Password Card
            <table>
                <tr>
                    <td>no</td>
                    <td>不使用</td>
                </tr>
                <tr>
                    <td>optional</td>
                    <td>部份使用</td>
                </tr>
                <tr>
                    <td>all</td>
                    <td>全部使用</td>
                </tr>
            </table>
        </td>
    </tr>
    <tr>
        <td>isFirstRun</td>
        <td>Boolean</td>
        <td>is available at first selection.</td>
    </tr>
    <tr>
        <td>isPreSelect</td>
        <td>Boolean</td>
        <td>will be selected for student before first selection.</td>
    </tr>
    <tr>
        <td>teachers</td>
        <td>String Array</td>
        <td>teacher names</td>
    </tr>
    <tr>
        <td>credit</td>
        <td>Number</td>
        <td>credit</td>
    </tr>
    <tr>
        <td>classRooms</td>
        <td>String[]</td>
        <td>class room number with building code</td>
    </tr>
    <tr>
        <td>times</td>
        <td>Object</td>
        <td>Key : Day of Week
            <table>
                <tr>
                    <td>0</td>
                    <td>Monday</td>
                </tr>
                <tr>
                    <td>1</td>
                    <td>Tuesday</td>
                </tr>
                <tr>
                    <td>2</td>
                    <td>Wednesday</td>
                </tr>
                <tr>
                    <td>3</td>
                    <td>Thursday</td>
                </tr>
                <tr>
                    <td>4</td>
                    <td>Friday</td>
                </tr>
                <tr>
                    <td>5</td>
                    <td>Saturday</td>
                </tr>
                <tr>
                    <td>6</td>
                    <td>Sunday</td>
                </tr>
            </table>
            Value : array of period(s)
            <table>
                <tr>
                    <td>sequences</td>
                    <td>1,2,3,4,Z,5,6,7,8,9,A,B,C,D,E,F</td>
                </tr>
            </table>
        </td>
    </tr>
    <tr>
        <td>type</td>
        <td>Enum</td>
        <td>
            <table>
                <tr>
                    <td>required</td>
                    <td>必修</td>
                </tr>
                <tr>
                    <td>elective</td>
                    <td>選修</td>
                </tr>
            </table>
        </td>
    </tr>
    <tr>
        <td>fullHalf</td>
        <td>Enum</td>
        <td>half year(1 semester) or full year(2 semesters)
            <table>
                <tr>
                    <td>full</td>
                    <td>全</td>
                </tr>
                <tr>
                    <td>half</td>
                    <td>半</td>
                </tr>
            </table>
        </td>					
    </tr>
    <tr>
        <td>maxStudents</td>
        <td>Number</td>
        <td>maximum amount of students, 0 means infinity.</td>
    </tr>
</table>

## Example
```json
[
	{
        "serialNo" : 12034,
        "no" : "EL5001",
        "classNo" : "*",
        "name" : "文學/文化理論導讀",
        "isClosed" : false,
        "memo": "限三、四年級",
        "isMasterDoctor": false,
        "language": "國語",
        "passwordCard": "不使用",
        "isFirstRun": true,
        "isPreSelect": true,
        "teachers": [  "錢夫人", "阿土伯" ],
        "credit": 2,
        "classRooms": [ "C2-209", "C2-209" ],
        "times": {
                  "0": ["5"],
                  "2": ["3", "4"]
                },
        "type": "必修",
        "fullHalf": "全",
        "maxStudents": 0
    }
]
```