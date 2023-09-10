# FRODY 
## Inspiration
According to the Federal Trade Commission (FTC), credit fraud is the most common form of identity fraud.  The increasing volume and frequency of trade pose a difficult challenge for firms in financial services to analyze real-time data to detect fraudulent transactions. A scalable and distributed data solution allows these business users to alert their customers, assuring the users that their transactional information is managed securely. 

## What it does
Frody is a microservice on the Google Cloud Platform that uses machine learning to flag and inform users on real-time transactional data. The user can "subscribe" to the transactional activities for multiple cards on a centralized dashboard, where they can monitor their transactional activities. If suspicious activity is detected with Frody's fraud detection model,  the users will be informed via text message immediately. 

## How we built it
We simulated real-time messaging service with Google Cloud Pub/Sub, using Java Spring Boot as a server-side application to stream randomly generated transactional data. Once the consumer of Pub/Sub persists the message to the Google Big Query database, then the message is checked for fraud via the machine learning model. If a fraudulent transaction is detected, the user will receive the transaction information on their phone via Twilio. Lastly, our centralized dashboard where users can "subscribe" to and monitor transactional activities for multiple cards is built using React.

## Challenges we ran into
We had to learn how to use services of Google Cloud Platform and Twilio. These services brought us much difficulty as creating a microservice on GCP was not as simple as we thought. 

## What's next
A future development would be to further optimize our machine learning model for even more accurate detection of suspicious activity. We also intend to expand our microservice to other transaction methods such as digital wallets and cryptocurrency wallets. 
