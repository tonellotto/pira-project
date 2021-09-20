# Distributed Personal Information Recognition system using gRPC

This project aims at:

1. identify, classify and link information relating personal data of sensitive nature (proper names, city names, identification codes, geographical coordinates) in textual documents
2. effectively and efficiently anonymize the identified personal data, according to their nature, keeping the statistical value of the data unchanged.

To achieve this goal, the technologies used were:
1. [Microsoft Presidio](https://microsoft.github.io/presidio/) for Data Protection and Anonymization
2. [gRPC](https://github.com/grpc/grpc) an open source universal RPC framework used to encapsulate the Microsoft Presidio modules (the Analyzer and the Anonymizer)

## Getting started

The project constist of two folders, one for the analyzer and one for the anonymizer. In each folder we can find the `proto` folder which contains a file called `model.proto` used to generate the needed stubs to create the gRPC client/server (`model_pb2.py` and `model_pb2_grpc.py`), the `analyzer-temp`/`anonymizer-temp` folder used by the server to save temporary files and four python files. For example in the case of the anonymizer: 
1. anonymizer_server.py - used to implement the gRPC server
2. anonymizer_client.py - used to implement the gRPC client
3. data_loader.py - a python program to use the functionality of the anonymizer (setup a configuration, perform anonymization/deanonymization)
4. clientGUI.py - a graphical user interface

The `analyzer-results` folder and the `anonymizer-results` folder are used to contain the respective results generated by the Microsoft Presidio modules.

For instructions on how to use.
* [Microsoft Presidio Analyzer](https://github.com/biagiocornacchia/microsoft-presidio/blob/main/analyzer/README.md)
* [Microsoft Presidio Anonymizer](https://github.com/biagiocornacchia/microsoft-presidio/blob/main/anonymizer/README.md)
