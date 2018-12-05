# maintenance

Automated Scheduled Maintenance events

## Setup

1. Fork this repo and clone it
2. Create a new maintainance yaml file
3. Open a new PR
4. Once merged, the new status should be created on our [statuspage].

## Creating a new scheduled maintenance event

Create a new yaml file on this repo following the `YYYY-MM-DD-name.yaml`
pattern.

### Maintainance file structure

Maintainance files are super simple data structures. By default, the only fields 
you'll need to worry about are `scheduled_for` and `scheduled_until`.

| Key             | Description                                            | Default value                                            |
| ---             | ---                                                    | ---                                                      |
| `name`          | (optional) The name for this maintenance event.        | String - `Scheduled maintenance`                         |
| `message`       | (optional) The description for this maintenance event. | String - `We'll be rolling updates to our web services.` |
| `scheduled_for` | Start date for the event.                              | String - `2018-12-04 7:00 PM`                            |
| `duration`      | Planned duration for the event.                        | String - `1 hour`                                        |
| `components`    | Any of our Status Page's components affected.          | Array - `pager.com`, `Billing API`                       |

[statuspage]: https://status.pager.com
