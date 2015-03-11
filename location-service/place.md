# Find Landscapes, Buildings or Faculties.

```
GET /place
```

## Description
> Find location of landscapes, buildings or faculties by query parameters.

# Request
## Headers
<table>
  <tr>
    <td><b>Name</b></td>
    <td><b>Required</b></td>
    <td><b>Description</b></td>
  </tr>
  <tr>
    <td><b>X-API-NCU-TOKEN</b></td>
    <td><i>yes</i></td>
    <td>Your public API token</td>
  </tr>
</table>
## Query Parameters
<table>
  <tr>
    <td><b>Name</b></td>
    <td><b><b>Required</b></b></td>
    <td><b>Description</b></td>
  </tr>
  <tr>
	<td><b>type</b></td>
	<td><i>no</i></td>
	<td>place type</td>
  </tr>
  <tr>
	<td><b>name</b></td>
	<td><i>no</i></td>
	<td>place's full Chinese name</td>
  </tr>
  <tr>
	<td><b>limit</b></td>
	<td><i>no</i></td>
	<td>1 &lt;= limit &lt;= 50, defaults to 5.</td>
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
		<td>無障礙坡道</td>
	</tr>
	<tr>
		<td>DISABLED_CAR_PARKING</td>
		<td>無障礙汽車位</td>
	</tr>
	<tr>
		<td>DISABLED_MOTOR_PARKING</td>
		<td>無障礙機車位</td>
	</tr>
	<tr>
		<td>EMERGENCY</td>
		<td>緊急</td>
	</tr>
	<tr>
		<td>AED</td>
		<td>AED 自動體外心臟電擊去顫器</td>
	</tr>
	<tr>
		<td>RESTAURANT</td>
		<td>餐廳</td>
	</tr>
	<tr>
		<td>SPORT_RECREATION</td>
		<td>休閒生活</td>
	</tr>
	<tr>
		<td>ADMINISTRATION</td>
		<td>行政服務</td>
	</tr>
	<tr>
		<td>RESEARCH</td>
		<td>教學研究</td>
	</tr>
	<tr>
		<td>DORMITORY</td>
		<td>宿舍</td>
	</tr>
	<tr>
		<td>OTHER</td>
		<td>其他單位</td>
	</tr>
	<tr>
		<td>ATM</td>
		<td>提款機</td>
	</tr>
	<tr>
		<td>BUS_STATION</td>
		<td>公車站牌</td>
	</tr>
	<tr>
		<td>PARKING_LOT</td>
		<td>停車場</td>
	</tr>
</table>

## Example
```
GET /place?type=AED
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
                    <td>place's Chinese name</td>
                </tr>
                <tr>
                    <td>englishName</td>
                    <td>String</td>
                    <td>place's English name</td>
                </tr>
				<tr>
					<td>type</td>
					<td>Enum</td>
					<td>Place Type</td>
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
			"chineseName" : "AED 自動體外心電擊去顫器",
			"englishName" : "AED, Automated External Defibrillator",
			"type" : "AED",
			"location" : {
				"lat" : 24.968275,
				"lng" : 121.195092
			}
		}, 
		{
			"chineseName" : "AED 自動體外心電擊去顫器",
			"englishName" : "AED, Automated External Defibrillator",
			"type" : "AED",
			"location" : {
				"lat" : 24.966139,
				"lng" : 121.19463
			}
		}, 
		{
			"chineseName" : "AED 自動體外心電擊去顫器",
			"englishName" : "AED, Automated External Defibrillator",
			"type" : "AED",
			"location" : {
				"lat" : 24.968501,
				"lng" : 121.19368
			}
		}, 
		{
			"chineseName" : "AED 自動體外心電擊去顫器",
			"englishName" : "AED, Automated External Defibrillator",
			"type" : "AED",
			"location" : {
				"lat" : 24.970142,
				"lng" : 121.192831
			}
		}, 
		{
			"chineseName" : "AED 自動體外心電擊去顫器",
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
