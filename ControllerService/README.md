# ControllerService

## Usage

`GET /timers`

Returns all timers.

**Response**

```json
{
    "tid":
    {
	    "alias": "String",
	    "uuid": "IP of device",
        "is_online": "Integer value, 1 if on, 0 if off",
        "tid": "Integer value, ID of timer",
        "time": "String, time formatted as HH:MM",
        "date": "String, formatted as DD.MM.YYYY, field not required",
        "status": "String, the desired action to be taken, i.e. on to turn on, off to turn off",
        "comment": "String, comment field",
        "deletable": "Integer value, 0 if not deletable otherwise deletable"
    }
}
```

`GET /alias/<alias>`

Returns first timer with the given alias. If no timers exist for given alias, returns 404.

**Response**

```json
{
	"alias": "String",
	"uuid": "IP of device",
    "is_online": "Integer value, 1 if on, 0 if off",
    "tid": "Integer value, ID of timer",
    "time": "String, time formatted as HH:MM",
    "date": "String, formatted as DD.MM.YYYY, field not required",
    "status": "String, the desired action to be taken, i.e. on to turn on, off to turn off",
    "comment": "String, comment field",
    "deletable": "Integer value, 0 if not deletable otherwise deletable"
```

`POST /create?alias=<ALIAS>&uuid=<IP-ADDRESS>&is_online=<0|1>&time=<HH:MM>&date=<DD.MM.YYYY>&status=<off|on>&comment=<STRING>&deletable=<INTEGER>"`

**Response**

- `200 OK` on success


If something is missing, no error handling is currently implemented:

```json
{
    "message": "Internal Server Error"
}
```
`GET /remove/<tid>`

**Response**
- `null`