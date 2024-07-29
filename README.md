# SALES DATA PROJECTION
Realtime Stream processing - Analysing the realtime sales data for the multiple gadgets

## TECHNOLOGIES

| S.No | TECH                                   | Services Used                          |
|------|----------------------------------------|----------------------------------------|
| 1    | Source                                 | Python mock data                       |    
| 2    | NoSQL DB                               | AWS DynamoDB                           |
| 3    | CDC                                    | DynamoDB Streams                       |
| 4    | Stream Ingestion                       | Event Bridge Pipe                      |
| 5    | Messaging Queue                        | Kinesis Streams                        |
| 6    | Batching the realtime data             | Kinesis Firehose                       |
| 7    | Transformation                         | AWS Lambda                             |
| 8    | Target                                 | AWS S3                                 |
| 9    | Analysis                               | AWS Athena                             |

## ARCHITECTURE

![Pipline_Architecture_Diagram](https://github.com/mohanprasath-de/sales-data-projection-realtime-streaming/blob/main/SalesData_architecture.png)

## EXPLANATION

1. Sales gadget data is generated using a Python mock data generator.
2. The data is stored in a DynamoDB table.
3. DynamoDB Streams is used for Change Data Capture to capture updates.
4. Kinesis Streams is used as a messaging queue.
5. DynamoDB Streams and Kinesis Streams are connected using an Event Bridge pipe (stream ingestion).
6. The real-time data is batched using Kinesis Firehose.
7. The transformation layer is scripted using a Lambda function.
8. The transformed data is stored in AWS S3 for future analysis using Athena.
