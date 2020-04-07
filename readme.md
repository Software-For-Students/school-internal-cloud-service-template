# Todo after cloning
- [ ] add description
- [ ] redo readme (using the description)
- [ ] rename root project name in settings.gradle
- [ ] rename package (template) to use service name
- [ ] delete gitkeep file in package path
- [ ] add develop branch
- [ ] setup branch protection rules

# API Routes

## /heartbeat/

|  Method   | Requires Data? | Data Format |  HTTP Response (Success)   | Response Data |
| :-------: | :------------: | :---------: | :------------------------: | :-----------: |
|   `GET`   |       no       |      -      |         `200` (OK)         |       -       |
| All other |       no       |      -      | `405` (Method not allowed) |       -       |

## /discovery/

|  Method   | Requires Data? | Data Format |  HTTP Response (Success)   |   Response Data    |
| :-------: | :------------: | :---------: | :------------------------: | :----------------: |
|   `GET`   |       no       |      -      |         `200` (OK)         | `application/json` |
| All other |       no       |      -      | `405` (Method not allowed) |         -          |

### GET /discovery/

Returns an json object string of containing the following elements:

|  Field Name   | Value Type | Value                                      |
| :-----------: | :--------: | :----------------------------------------- |
| `serviceName` |  `String`  | The registered name of the service         |
|  `serviceId`  |   `int`    | The registered id number of the service    |
|  `workerId`   |   `int`    | The worker id of the request handling node |