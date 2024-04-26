# mule-servicenow-implementation
Use Mule 4 Service Now connector to create and retrieve Incidents

## About Project
Create, retrieve incidents from Service Now Instance using Mule 4 Service Now Connector
Uses HTTP basic authentication to connect with Service Now Instance.

## About Service Now
ServiceNow is used to set up systems that define, manage, automate and structure IT services for companies. At a very simple level, it as a tool that allows you to raise and track tickets as well as process and catalogue regular IT service requests.

## Setting Up Prerequisites
Step 1: Go to https://developer.servicenow.com/ Click on Sign up and start building.
Step 2: Request a developer instance. Go to 'manage the Instance password' and copy URL, username, password which will be used in mule configuration.

## Using Mulesoft Application
- Use service now instance credentials in config.
- Debug project in local.
- Goto http://localhost:8081/snow/create and observe below response.
```
{
  "headers": {
  },
  "attachments": {
  },
  "body": {
    "insertResponse": {
      "sys_id": "26bbd831c37182108fecbbec0501311b",
      "number": "INC0010001"
    }
  }
}
```
- Goto http://localhost:8081/snow/retrieve and observe response in below format.
```
{
  "headers": {
    
  },
  "attachments": {
    
  },
  "body": {
    "getRecordsResponse": {
      "getRecordsResult": {
        "active": "0",
        "activity_due": "2016-12-13 01:26:36",
        "additional_assignee_list": null,
        "approval": "not requested",
        "approval_set": null,
        "assigned_to": "5137153cc611227c000bbd1bd8cd2007",
        "assignment_group": "287ebd7da9fe198100f92cc8d1d2154e",
        "business_duration": "1970-01-01 08:00:00",
        "business_impact": null,
        "business_service": "27d32778c0a8000b00db970eeaa60f16",
        "business_stc": "28800",
        "calendar_duration": "1970-01-02 04:23:17",
        "calendar_stc": "102197",
        "caller_id": "681ccaf9c0a8016400b98a06818d57c7",
        "category": "inquiry",
        "cause": null,
        "caused_by": null,
        "child_incidents": "0",
        "close_code": "Solved (Permanently)",
        "close_notes": "This incident is resolved.",
        "closed_at": "2016-12-14 02:46:44",
```
