# PHP Engineer Challenge
This page outlines the coding challenge required for prospective PHP engineers at MyDoc

# Purpose
The aim of this challenge is to get an understanding of how you think and how that translates into working code. 

# What we are looking for

- Coding standard, comments and style
- Documentation
- Unit testing strategy
- Overall solution design
- Appropriate use of source control

# Challenge

Your challenge is to build a version controlled REST API Calculator. 

This calculator API  must be able to perform the following operations for a reasonable number of concurrent users.

- [Addition](#addition)
- [Subtraction](#subtraction)
- [Division](#division)
- [Multiplication](#multiplication)
- [Square Root](#square-root)
- [Save Value](#save-value)
- [Retrieve Value](#retrieve-value)
- [Clear Value](#clear-value)

All answers and errors should be returned in the response format described below. 

## Technical Requirements

### Addition

This endpoint should allow the addition of 2 values

Method: `POST`

Endpoint: `/add`

Body: 
```json
 {"num1":  1, "num2": 2}
```

Response
```json
{"answer": 3}
```
  

### Subtraction

This endpoint should allow the subtraction of 2 values

Method: `POST`

Endpoint: `/subtract`

Body: 
```json
 {"num1":  10, "num2": 4}
```

Response
```json
{"answer": 6}
```

### Multiplication
This endpoint should allow the multiplication of 2 values

Method: `POST`

Endpoint: `/multiply`

Body: 
```json
 {"num1":  7, "num2": 5}
```

Response
```json
{"answer": 35}
```

### Division
This endpoint should allow the division of 2 values

Method: `POST`

Endpoint: `/divide`

Body: 
```json
 {"num1":  81, "num2": 9}
```

Response
```json
{"answer": 9}
```

### Square Root
This endpoint should return the square root of a value

Method: `POST`

Endpoint: `/squareRoot`

Body: 
```json
 {"num1":  61}
```

Response
```json
{"answer": 7.8102}
```

### Save Value
This endpoint should allow the user to save a value for later use. 

Method: `POST`

Endpoint: `/save`

Body: 
```json
 {"value": 12}
```

Response
```json
{"save": true}
```

### Retrieve Value
This endpoint should return the saved value

Method: `GET`

Endpoint: `/savedValue`

Response
```json
{"value": 12}
```

### Clear Value
This endpoint should clear the saved value

Method: `POST`

Endpoint: `/clear` 

Response
```json
{"value": null}
```

## Error Handling

All errors must return the appropriate HTTP status code. 
Error messages should be returned with the following format.

```json
{"error":  "The error message"}
```


## Guidelines

- Use Laravel for building the API
- Use PHP 7.2
- Deploy this to a server and give us the URL.
- Push the code to a public git repository and give us the URL.
  - Your repository should include the following
    - Source Code
    - Documentation
    - Test Cases (Along with instructions on how to execute the test cases)
- You are free to use any open source database or library.

## Note
We are NOT judging for algorithmic brilliance or cool one liners. We want to see if you can write production quality code. So please build this assuming you are building a production quality service.


