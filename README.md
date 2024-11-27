# Data_Cleaning_Code_for_BigDataProject
Code for data cleaning and pre-processing for  product data

TOOLS USED:		PYTHON FOR DATA CLEANING AND PRE-PROCESSING APACHE PIG FOR DATA ANALYSIS

DATASOURCE: KAGGLE
https://www.kaggle.com/hetulmehta/bigbasket-products-dataset SCHEMA:
PRODUCT, CATEGORY, SUB-CATEGORY, BRAND, TYPE, RATING, SALE_PRICE, MARKET_PRICE, PROFIT, PROFIT%
SIZE: 22.45 MB



DATA CLEANING IN PYTHON
•	UNECCESSARY COLUMNS LIKE URLS, CODES WERE REMOVED
•	NULL VALUES AND DUPLICATES WERE REMOVED
•	MISSING VALUES IN RATING COLUMNS WE REPLACED WITH ITS MEDIAN.
DETAILED EXPLANATION IN JUPYTER NOTEBOOK
 

   
 

ANALYSIS PART USING PIG
1) LOAD, DESCRIBE AND DUMP OPERATIONS

<img width="465" alt="image" src="https://github.com/user-attachments/assets/a6b97231-6bf2-4781-9363-b2f00d0b2048">


DUMPED DATA
 
 
<img width="447" alt="image" src="https://github.com/user-attachments/assets/b6b2f626-9db1-4f41-8778-b2912341dd06">






QUERIES:
1)	MAXIMUM RATED PRODUCTS: THAT IS PRODUCTS WITH RATING 5
<img width="451" alt="image" src="https://github.com/user-attachments/assets/1f14e442-4141-435b-b9bc-d60466d19fb5">



OUTPUT:
 
 <img width="450" alt="image" src="https://github.com/user-attachments/assets/c7ed745a-bd31-45e5-a1f4-4253b85c94e8">
<img width="456" alt="image" src="https://github.com/user-attachments/assets/f36b5e33-44b0-48f7-8f37-f4cc03da76d3">



FROM THE OUTPUT WE CAN SEE THAT THE HIGHEST RATED PRODUCTS ARE : DRINKS(TEA) , SANITARY PRODUCTS AND PRODUCTS FOR BABIES LIKE TISSUES, DIAPERS ETC.



2)	MINIMUM RATED PRODUCTS: THAT IS PRODUCTS WITH RATING 1

<img width="450" alt="image" src="https://github.com/user-attachments/assets/4c42bcd1-4f6d-448c-9e1a-714defb20438">





OUTPUT:
 
 <img width="460" alt="image" src="https://github.com/user-attachments/assets/c3be5a6e-1c4b-4927-a0c4-78fe4e240e53">




FROM THE OUTPUT WE CAN SEE THAT THE LEAST RATED PRODUCTS ARE : BEAUTY ,SKIN-CARE AND HYGEIENE TYPE PRODUCTS AND SOME FOOD ITEMS.





3)	NUMBER OF PRODUCTS PER BRAND:
	<img width="450" alt="image" src="https://github.com/user-attachments/assets/94b25ec1-f460-4ba4-a2d8-ceecbbff974a">


OUTPUT:
 <img width="149" alt="image" src="https://github.com/user-attachments/assets/bff606cc-45a0-4bf1-9fd1-71927365339a">

 


FROM THE OUTPUT WE CAN SEE BRAND WISE COUNT OF PRODUCTS.
BRANDS like FRESHO , BBHOME ,COLGATE ETC.HAVE MORE NO. OF PRODUCTS.


4)	TOTAL PROFIT MADE BY EACH BRAND
 

 <img width="256" alt="image" src="https://github.com/user-attachments/assets/e9f881bd-d64b-4fe3-814c-03adc17f530f">



OUTPUT:
 <img width="385" alt="image" src="https://github.com/user-attachments/assets/ac7912a7-6e5c-4379-ac95-fb9e31f50c4e">

 



TOTAL PROFIT MADE BY EACH BRAND IN RUPEES IS SHOWN IN THE OUTPUT.

5)	AVERAGE RATING PER BRAND
 
 <img width="426" alt="image" src="https://github.com/user-attachments/assets/c269debc-29bd-496d-88bb-c24d0ee48873">


OUTPUT:
<img width="151" alt="image" src="https://github.com/user-attachments/assets/7a99d4ce-b153-4b9a-82c4-4c0dc968323d">



AVERAGE RATING PER BRAND IS SEEN IN THE OUTPUT I.E OUTPUT RATINGS IN THE RANGE(1-5)
 
BRANDS LIKE OREO ,TANG HAVE AVERAGE RATING 4 AND BRANDS LIKE MARS AND NICE HAVE AVERAGE RATING 5



6)	MOST PROFITABLE PRODUCT
<img width="337" alt="image" src="https://github.com/user-attachments/assets/9819bdcf-f1a1-49cb-b482-72719d5db9fd">


OUTPUT:
<img width="449" alt="image" src="https://github.com/user-attachments/assets/baccee6b-070f-426e-a1a6-1ae74eea1b0a">


FROM THE OUTPUT WE CAN SEE THE MOST PROFITABLE PRODUCT IS PREMIUM CLOTH DRYER FROM THE BRAND DP


7)	LEAST PROFITABLE PRODUCTS
   <img width="331" alt="image" src="https://github.com/user-attachments/assets/53679357-e313-430a-b6db-197be9d0818d">


OUTPUT:
 <img width="473" alt="image" src="https://github.com/user-attachments/assets/f800e4a1-53cd-4bdd-8804-24424c5e93d9">

 

FROM THE OUTPUT WE CAN SEE THE PRODUCTS WITH 0 RUPEES PROFIT AND THESE ARE MOSTLY THE PRODUCTS THAT FALL IN THE CATEGORY OF HOUSEHOLD/CLEANING ETC.

8)	MOST EXPENSIVE PRODUCT
<img width="450" alt="image" src="https://github.com/user-attachments/assets/c37a0f10-16d1-4c03-9eb6-d8737754ef7a">


OUTPUT:
<img width="449" alt="image" src="https://github.com/user-attachments/assets/91cf362b-334d-425b-af4a-5285aa816c2e">


FROM THE OUTPUT WE CAN SEE EPILATOR IS THE MOST EXPENSIVE PRODUCT AS PER SALE PRICE.


9)	CHEAPEST PRODUCT
 
 <img width="455" alt="image" src="https://github.com/user-attachments/assets/f164549a-d50f-4c76-8b00-d664cf882ce3">


OUTPUT:
<img width="451" alt="image" src="https://github.com/user-attachments/assets/b0b765dd-a5ac-4227-845e-bb8ee45b7380">

FROM THE OUTPUT THE CHEAPEST PRODUCT IS FOUND TO BE CURRY LEAVES


10)	NUMBER OF PRODUCTS PER TYPE
    <img width="453" alt="image" src="https://github.com/user-attachments/assets/9c3a96fb-88d4-4057-809f-d5c6832b02e5">


OUTPUT:
 
 <img width="247" alt="image" src="https://github.com/user-attachments/assets/f70eac88-ca03-42f4-8191-e92db7925547">




FROM THE OUTPUT WE CAN SEE COUNT BY TYPE
FACE CARE , SHAMPOO ,HANDWASH HAVE HIGH NUMBERS.



CONCLUSION:
 
MOST PROFITABLE CATEGORIES ARE:
BEAUTY & HYGIENE
Comparatively fruits and vegetables and cleaning products are least profitable
So marketing and advertising or discounts can be added
And low rated products like cleaning and household should be also taken care using similar strategies in order to increase sales and profit.
![image](https://github.com/user-attachments/assets/f895cad9-869f-47a8-8cba-59ec70cf184f)
