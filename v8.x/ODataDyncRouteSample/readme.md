It's a customer sample project that needs to investigate.

### 08-30-2024

```C#
http://localhost:5043/api/v2/Azure
```

It returns:
```json
{
    "@odata.context": "http://localhost:5043/api/v2/$metadata#Azure",
    "value": [
        {
            "ProductCategories": [],
            "UpdateTypes": [],
            "Id": "1",
            "Title": "Azure Update 1",
            "Description": "Azure Update 1 Description",
            "Status": null,
            "Created": "0001-01-01T00:00:00-08:00",
            "Modified": "0001-01-01T00:00:00-08:00",
            "Products": [],
            "Content": "a string value here",
            "otherdata": true,
            "Availabilities": []
        },
        {
            "ProductCategories": [],
            "UpdateTypes": [],
            "Id": "2",
            "Title": "Azure Update 2",
            "Description": "Azure Update 2 Description",
            "Status": null,
            "Created": "0001-01-01T00:00:00-08:00",
            "Modified": "0001-01-01T00:00:00-08:00",
            "Products": [],
            "Availabilities": []
        }
    ]
}
```

More, 
```C#
http://localhost:5043/api/v2/Azure?$filter=Id eq '2'
```

It returns:
```json
{
    "@odata.context": "http://localhost:5043/api/v2/$metadata#Azure",
    "value": [
        {
            "ProductCategories": [],
            "UpdateTypes": [],
            "Id": "2",
            "Title": "Azure Update 2",
            "Description": "Azure Update 2 Description",
            "Status": null,
            "Created": "0001-01-01T00:00:00-08:00",
            "Modified": "0001-01-01T00:00:00-08:00",
            "Products": [],
            "Availabilities": []
        }
    ]
}
```

More:

```C#
http://localhost:5043/api/v2/Azure?$filter=Id eq '2'&$select=Created,Modified
```

It returns:


```json
{
    "@odata.context": "http://localhost:5043/api/v2/$metadata#Azure(Created,Modified)",
    "value": [
        {
            "Created": "0001-01-01T00:00:00-08:00",
            "Modified": "0001-01-01T00:00:00-08:00"
        }
    ]
}
```
