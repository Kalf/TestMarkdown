# List of time plans
___
##Description
This status returns a comma separated list of time plans avalable in the TLC.

+ **ObjectType:** Traffic Controller
+ **Object:** 
+ **StatusCodeId:** S0022
+ **Description:** List of time plans

## Return value
+ **Name:** Status
+ **Type:** String
+ **Value:** [text]
+ **Comment:** Comma spearated list of configured time plans

### Definition of return string
The return string is defined as;

```
n,n,n
```

Where:

| legend | description |
| ------- | ---------- |
| n | index of timeplan |

**Note!**
The length of the string, (I.e. number of parameters in string) is defined by number of avalable time plans in the TLC.
**Note 2!**
All time plans are separated with a comma (,)

## Example message

**Status request**
``` json
	{"mType":"rSMsg",
		"type":"StatusRequest",
		"mId":"4d5dcb2e-7f5d-4c87-a186-a2c466dafd3b",
		"ntsOId":"AA+BBCCC=DDDEEFFF",
		"xNId":"",
		"cId":"AA+BBCCC=DDDEEFFF",
		"sS":[{"sCI":"S0022",
		"n":"status"}]}
```

**Status Response**
``` json
	{"mType":"rSMsg",
		"type":"StatusResponse",
		"mId":"339319bd-9c4e-4318-b34f-851d41ee7bd1",
		"ntsOId":"AA+BBCCC=DDDEEFFF",
		"xNId":"",
		"cId":"AA+BBCCC=DDDEEFFF",
		"sTs":"2016-05-11T09:55:07.712Z",
		"sS":[{"sCI":"S0022",
		"n":"status",
		"s":"1,2,3,5",
		"q":"recent"}]}

```

**Note!**
All messages should be acknowledged by the other part (The SCADA acknowledges the TLC's messages and vice versa). The acknowledg messages are not presented in the above examples. For more information see the RSMP specification.
