# PHP-DBDesign-Implement-CheckTransactionTracking
Database design and implemeting the screen that users can record checks, give to currents for payment, receive payment from bank/lawyer and track all their movements. Some parts of the project are binded to other Controller.php or Model.php files (for example: Bank List for payment,Current list, lawyer list. ) Description of the project and screenshots here. Since this project is currently used by the company(MomentumSoft), source codes are private for security issues. You can send me an email for the share source code repository.

This project was developed using the PHP Codeigniter framework in accordance with the Model-View-Controller structure.

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

recording customer check. Current Directory on "Cari Seçimi" is dynamically pulled from database. This directory shows all the currents that users have according to logged user. : ![check1](https://user-images.githubusercontent.com/82888052/158999069-a994cb6b-5c92-48ee-b990-2929bdd1df2b.png)
when we click the "Save/Update" button on the tab. ![check2](https://user-images.githubusercontent.com/82888052/158999164-024f2a06-d389-42ad-938a-bbdee51241e6.jpg)

then we are directed to main page that all check exist. if we want to update, delete or do check transaction, ve click de "DÜZENLE/HAREKETLERİ GÖR" button on the "İŞLEMLER" tab.
And  when we clicked the edit button , this buttons on "İŞLEMLER" tab are coming according to Check State. if chkeck in "PÖRTFÖYDE" state that means we can do this transactions on the check.
![carirehber6](https://user-images.githubusercontent.com/82888052/158999614-954c288d-3fc7-45ac-b564-135ceaf61146.png)

In order to test, when we click "BANKA TAHSİLE VER" button for send check to bank payment, this pop up model will open:![checkbankpayment](https://user-images.githubusercontent.com/82888052/158999960-b4decc39-b503-4714-b646-cd67ea995734.jpg)

When we click the "BANKA SEÇ" button Bank Directory model will open for show users saved banks. The user can select the bank from which the check will be payment : 


![bankrehber](https://user-images.githubusercontent.com/82888052/159000309-ef068780-d3f0-4377-baae-38856a1429e6.jpg)

after select:
![bankrehber3](https://user-images.githubusercontent.com/82888052/159000342-1c88accb-8f6e-4253-8907-28f9bd60a681.jpg)


then we can see the check state is changed. The check can't be editted right now because we send check to bank payment. We can mark this check "BANKA TAHSİL EDİLDİ" if we get the payment(and bank payment process will be doing right now)  or we can send check back to portfolio for another transaction.
![bankrehber4](https://user-images.githubusercontent.com/82888052/159000427-921c84c9-f4b2-4d5c-9676-6a0b303fd04d.jpg)

if we try to delete check, we can't do that. We tell the user what he/she can do : ![bankrehber6](https://user-images.githubusercontent.com/82888052/159001010-1fc4ffd0-2f92-449d-8a7d-b4c484a3baeb.jpg)
and we can send check back to portfolio(Click the "PÖRTFÖYE GERİ AL" button) for do another transaction.![bankrehber8](https://user-images.githubusercontent.com/82888052/159001251-89a5175e-c773-4bfc-917e-db7b4fb2d012.jpg)
![bankrehber9](https://user-images.githubusercontent.com/82888052/159001262-80dd05f3-679d-410a-8561-f2254024c610.jpg)

then we can give the check another current now. When we click the "CİROLA" button current directory pop up will open.
![carirehber1](https://user-images.githubusercontent.com/82888052/159001517-b647488e-bf8e-4b12-8cdb-b9feff0e56fd.png)![carirehber2](https://user-images.githubusercontent.com/82888052/159001583-1a6bff5e-a8ab-46b7-a970-fe81beb5bd4a.png)
![carirehber3](https://user-images.githubusercontent.com/82888052/159001625-2edae95a-0bc0-41ed-ac32-457c2504aed3.png)
and as can we see, after we send check to current, check transactions we can do have changed:

![carirehber4](https://user-images.githubusercontent.com/82888052/159001774-c643d70a-992d-4e70-a305-97e8f6e7ca5e.png)

we will send check back to portfolio and we will mark the check as cash cashed.![carirehber5](https://user-images.githubusercontent.com/82888052/159001956-fb706191-e244-4aa5-9c0e-d311ddf4909b.png)

![carirehber6](https://user-images.githubusercontent.com/82888052/159001975-60c1810a-63c9-400a-b877-ab78a2fee623.png)



![nakittahsil1](https://user-images.githubusercontent.com/82888052/159002175-f6905f93-3eac-43e6-84cb-c096263f9d87.png)

 we can see the check's new state on main screen.


![nakittahsil2](https://user-images.githubusercontent.com/82888052/159002232-a3d8372d-2d3d-4e30-b989-b3a3d876295e.png)

now check is locked upbecause it was charged.
![nakittahsil3](https://user-images.githubusercontent.com/82888052/159002357-bb86ba9f-93a0-4f2e-ab1e-56d58889b879.png)

and as i said, we can see al check movements because all of this movements are saved in database that we design.


![çekhareketleri](https://user-images.githubusercontent.com/82888052/159002560-7e7af9d4-e7fb-4b26-95fa-4bbe9df129b1.png)


i summerized this project's doing. It's other functions ( Send check to lawyer, send check to bank assurance...) are also working properly and all records are in our database.

