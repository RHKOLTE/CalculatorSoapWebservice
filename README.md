# CalculatorSoapWebservice

MuleSoft Flow: Simple Calculator Web Service
This project demonstrates how to implement a basic calculator web service using MuleSoft. 
The service supports basic arithmetic operations such as addition, subtraction, multiplication, and division by utilizing a WSDL file to define the SOAP operations.

Steps to Implement the Flow
WSDL Selection
Use the following WSDL for the calculator service:
http://www.dneonline.com/calculator.asmx?WSDL

CXF Component Configuration

Import the WSDL into the Mule project.
Use the CXF component to auto-generate Java classes from the WSDL. These include:
com.calculator.CalculatorSoap (Interface)
com.calculator.CalculatorSoapImpl (Implementation class for operations like add, subtract, multiply, and divide)
Request and response classes for each operation.

Mule Flow Design

Use an HTTP Listener to expose the calculator service on a specified port, e.g., 8081.
Configure the CXF Inbound Endpoint to process incoming SOAP requests and route them to the appropriate operations.
Implement the operations in the CalculatorSoapImpl class.
Operation Logic Implementation

Define the logic for each operation (add, subtract, multiply, divide) in the CalculatorSoapImpl class.
Ensure the request and response objects are appropriately handled to generate XML responses.
Testing

Run the Mule project.
Access the WSDL at: http://localhost:8081/calculator?wsdl
Use SoapUI or any SOAP testing tool to send requests for the operations and verify responses.
Limitations

This project is a simple demonstration and does not include error handling for invalid inputs 
(e.g., division by zero or malformed requests).
Flow Diagram Overview
A high-level representation of the Mule flow:

HTTP Listener →
CXF Inbound Endpoint →
Operation Logic (Java Implementation) →
SOAP Response Generation
