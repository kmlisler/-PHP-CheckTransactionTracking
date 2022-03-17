# PHP-DBDesign-Implement-CheckTransactionTracking
Database design and implemeting the screen that users can record checks, give to currents for payment, receive payment from bank and track all their movements. Some parts of the project are binded to other Controller.php or Model.php files (for example: Bank List for payment,Current list, lawyer list. ) Description of the project and screenshots here. Since this project is currently used by the company(MomentumSoft), source codes are private for security issues. You can send me an email for the share source code repository.

This screens are used for check record/transactions tracking for each user. All currents and banks informations are pulled from database existing records/tables dynamically due to each user's id. All bank balance transactions are saved in database,but they are not processed now. This CheckCard and CheckMovements models in database creates the necessary infrastructure for processing movements and transactions.
Use Cases for Customer Check and Own Check

Customer Check :![Müşteri Çeki](https://user-images.githubusercontent.com/82888052/158776137-41144d04-ef9c-402a-b7e2-881a9ba7f48d.jpeg)

Own Check : 
![Kendi Çekim](https://user-images.githubusercontent.com/82888052/158776186-765306db-f7a4-466d-b610-541830009925.jpeg)


Database Model and Descriptions;
![Database Entity Relationship SON HAL](https://user-images.githubusercontent.com/82888052/158775472-61b1d25a-81fc-4936-8f40-950d6913f47f.PNG)

Main Check Screen( with some test records ) 

![main_screen](https://user-images.githubusercontent.com/82888052/158779006-c4ccb47b-2f1c-4cc9-9ff3-2eadd90dff83.jpg)

user can select type of the document. Inputs will come according to the selected document type : 
![belge_tipi](https://user-images.githubusercontent.com/82888052/158779655-9e0776f5-a93e-4b68-becd-ba0366a76df4.png)

screen for own check:![own_check](https://user-images.githubusercontent.com/82888052/158796066-3cdd0e61-8d9a-4968-90a9-859b6b80419c.jpg)

screen for customer check : ![customer_check](https://user-images.githubusercontent.com/82888052/158796092-912a9970-d3c4-4b62-adc9-65c4e8610c3c.jpg)



....to be continued

