# Terraform custom provider: Device42

## Description
This is a custom created terraform provider to be used to interact with the device42 API.

## Device Resource: Argument Reference
* name - (required) the server hostname (minus the domain)
* custom_fields - (optional) a hash (map) of custom fields and values that will be added to this device

## Examples:

```
provider "device42" {
  host     = "api.device42.com" #Optional
  username = "user1"            #Optional
  password = "pass1"            #Optional
}

resource "device42_device" "server-1" {
  name          = "server-1"    #Required
  custom_fields = {             #Optional
  	"bt_lob"   = "lob_1"        #Optional
  	"bt_owner" = "terraform"    #Optional
  }
}
```