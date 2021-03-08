# DeviceService 

## Usage

All responses will have the form

```json
{
	"data": "Mixed type holding the content of the response",
	"message": "Description of what happened"
}
```

Subsequent response definitions will only detail the expected value of the `data field´

### List all devices

**Definition**

`Get /devices`

**Response**

- `200 OK` on success

```json
{
  [
    [\"192.168.8.103\", \"7E\"],
    [\"192.168.8.105\", \"F6\"],
    [\"192.168.8.101\", \"DF\"],
    [\"192.168.8.104\", \"BE\"],
    [\"192.168.8.102\", \"CA\"]
  ]
}
```

