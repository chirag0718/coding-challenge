# Coding challenge
This page consists coding challenge for Backend Engineer role at MyDoc.

# Purpose
Aim of this test is three fold

- Evaluate your coding abilities 
- Judge your technical experince
- Understand how you design a solution

# How you will be judged
You will be scored on

- Coding standard, comments and style
- Unit testing strategy
- Overall solution design
- Appropriate use of source control

# Challenge

Build a version controlled key-value store with a HTTP API we can query that from. The API needs to be able to:
- Accept a key(string) and value(some json blob/string) {"key" : "value"} and store them. If an existing key is sent, the value should be updated
- Accept a key and return the corresponding latest value
- When given a key AND a timestamp, return whatever the value of the key at the time was.

Assume only GET and POST requests for simplicity.


## Explanation 

### GET
Endpoint  `/object/mykey`

Response 
```json
{
    "value": "value1"
}
```

### POST
Endpoint  `/object`

Body 
```json
{
    "mykey" : "value2"
}
```
Time: 6.05 pm

Response 
```json
{
    "key": "mykey",
    "value": "value2",
    "timestamp": "<time>"
}
```
- Where time is timestamp of the new value (6.05pm)

### GET
Endpoint  `/object/mykey`

Response 
```json
{
    "value": "value2"
}
```

### GET
Endpoint  `/object/mykey?timestamp=1440568980` 
- Notice that timestamp=1440568980 [6.03pm] here is not exactly 6.00pm

Response 
```json
{
    "value": "value1"
}
```
- still return value1 , because value2 was only added at 6.05pm
- All timestamps are unix timestamps according UTC timezone.

## Guidelines

- Use NodeJS for scripting the backend.
- Deploy this to a server and give us the URL.
- Push the code to a public git repository and give us the URL.
- You are free to use any open source database or library.

### A good submission will have the following characteristics
- Clean and extendable code
- Handle a wide variety of edge cases
- Not break under a reasonable load
- Show knowledge of the various testing methodology

## Note
We are NOT judging for algorithmic brilliance or cool one liners. We want to see if you can write production quality code. So please build this assuming you are building a production quality service.


