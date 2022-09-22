# NIM-Conn-System-REST-IMSGlobal-OneRoster
<p align="center">
<img src="https://user-images.githubusercontent.com/24281600/191794680-5b4ef3e4-9323-4d0a-9548-6fff0b020fc5.png" />
</p>


# Filtering
Default filters are any records with an "active" status
![image](https://user-images.githubusercontent.com/24281600/168872696-c211abdb-af4d-4fb5-975a-99b2911a1332.png)

Reference the documentation for additional parameters
- v1.1
  - http://www.imsglobal.org/oneroster-v11-final-specification#_Toc480451997

# Metadata
Metadata can be added by leverage the custom field modifications to the system. 
1. Create file in "C:\ProgramData\Tools4ever\NIM\config\rest\systems\" called OneRosterSystemNameHere.json
2. Define JSON for custom Fields. Example below

```
{
  "schema": {
    "crud_objects": {
      "users": {
        "resources": {
          "metadata": {
            "ic.legacySourcedId": "string*"
          }
        }
      },
      "results": {
        "resources": {
          "metadata": {
            "ext_infiniteCampus_assignmentRawScore": "string*",
            "ext_infiniteCampus_isAssignmentResult": "string*",
            "ext_infiniteCampus_schoolSourcedId": "string*"
          }
        }
      },
      "lineItems": {
        "resources": {
          "metadata": {
            "ext_infiniteCampus_isGradingWindowOpen": "string*",
            "ext_infiniteCampus_isOneTime": "string*",
            "ext_infiniteCampus_isStandard": "string*"
          }
        }
      },
      "demographics": {
        "resources": {
          "metadata": {
            "ic_address": {
              "city": "string*",
              "districtResidenceName": "string*",
              "districtResidenceNumber": "string*",
              "number": "string*",
              "sourcedId": "string*",
              "state": "string*",
              "street": "string*",
              "tag": "string*",
              "zipcode": "string*"
            },
            "ic_homePhone": "string*",
            "ic_cellPhone": "string*",
            "ic_workPhone": "string*"
          }
        }
      }
    }
  }
}
```

# Known Limitations
- Users > userProfiles > Credentials
  - Not currently available
- Metadata > Array Objects
  - Not currently available

# NIM Docs
The official NIM documentation can be found at: https://docs.nimsuite.com
