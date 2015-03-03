# Find By PlaceType

```
GET /place/type/{placeType}
```

## Description
> Find location of landscapes, buildings or faculties by place type.

# Request
## Parameters
<table>
  <tr>
    <td><b>Parameter</b></td>
    <td><b><b>Required</b></b></td>
    <td><b>Description</b></td>
  </tr>
  <tr>
    <td><b>token</b></td>
    <td><i>yes</i></td>
    <td>Your API token</td>
  </tr>
</table>
## Place Type
<table>
	<tr>
		<td>type</td>
		<td>description</td>
	</tr>
	<tr>
		<td>WHEELCHAIR_RAMP</td>
		<td>�L��ê�Y�D</td>
	</tr>
	<tr>
		<td>DISABLED_CAR_PARKING</td>
		<td>�L��ê�T����</td>
	</tr>
	<tr>
		<td>DISABLED_MOTOR_PARKING</td>
		<td>�L��ê������</td>
	</tr>
	<tr>
		<td>EMERGENCY</td>
		<td>���</td>
	</tr>
	<tr>
		<td>AED</td>
		<td>AED �۰���~��Ŧ�q���hŸ��</td>
	</tr>
	<tr>
		<td>RESTAURANT</td>
		<td>�\�U</td>
	</tr>
	<tr>
		<td>SPORT_RECREATION</td>
		<td>�𶢥ͬ�</td>
	</tr>
	<tr>
		<td>ADMINISTRATION</td>
		<td>��F�A��</td>
	</tr>
	<tr>
		<td>RESEARCH</td>
		<td>�оǬ�s</td>
	</tr>
	<tr>
		<td>DORMITORY</td>
		<td>�J��</td>
	</tr>
	<tr>
		<td>OTHER</td>
		<td>��L���</td>
	</tr>
	<tr>
		<td>ATM</td>
		<td>���ھ�</td>
	</tr>
	<tr>
		<td>BUS_STATION</td>
		<td>�������P</td>
	</tr>
	<tr>
		<td>PARKING_LOT</td>
		<td>������</td>
	</tr>
	<tr>
		<td></td>
		<td></td>
	</tr>
</table>

## Example
```
GET /place/type/AED
```

# Response

## Formats
- json

## Structure
<table>
    <tr>
		<td><b>Filed Name</b></td>
		<td><b>Type</b></td>
		<td><b>Value Description</b></td>
	</tr>
    <tr>
        <td>result</td>
        <td>list</td>
        <td>
			Result Object
            <table>
                <tr>
                    <td>chineseName</td>
                    <td>String</td>
                    <td>place's name in Chinese</td>
                </tr>
                <tr>
                    <td>englishName</td>
                    <td>String</td>
                    <td>place's name in English</td>
                </tr>
				<tr>
					<td>type</td>
					<td>Enum</td>
					<td>[Place Type](#place-type)</td>
				</tr>
                <tr>
                    <td>location</td>
                    <td>LatLng</td>
                    <td>
						LatLng Object
						<table>
							<tr>
								<td>lat</td>
								<td>Latitude</td>
							</tr>
							<tr>
								<td>lng</td>
								<td>Longitude</td>
							</tr>
						</table>
					</td>
                </tr>
            </table>
        </td>
    </tr>
</table>

## Example
```json
{
	"result" : 
	[
		{
			"chineseName" : "AED �۰���~�߹q���hŸ��",
			"englishName" : "AED, Automated External Defibrillator",
			"type" : "AED",
			"location" : {
				"lat" : 24.968275,
				"lng" : 121.195092
			}
		}, 
		{
			"chineseName" : "AED �۰���~�߹q���hŸ��",
			"englishName" : "AED, Automated External Defibrillator",
			"type" : "AED",
			"location" : {
				"lat" : 24.966139,
				"lng" : 121.19463
			}
		}, 
		{
			"chineseName" : "AED �۰���~�߹q���hŸ��",
			"englishName" : "AED, Automated External Defibrillator",
			"type" : "AED",
			"location" : {
				"lat" : 24.968501,
				"lng" : 121.19368
			}
		}, 
		{
			"chineseName" : "AED �۰���~�߹q���hŸ��",
			"englishName" : "AED, Automated External Defibrillator",
			"type" : "AED",
			"location" : {
				"lat" : 24.970142,
				"lng" : 121.192831
			}
		}, 
		{
			"chineseName" : "AED �۰���~�߹q���hŸ��",
			"englishName" : "AED, Automated External Defibrillator",
			"type" : "AED",
			"location" : {
				"lat" : 24.968258,
				"lng" : 121.191057
			}
		}
	]
}
```