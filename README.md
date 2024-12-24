# Performance Testing

# Project Description
<pre>
 I have performed performance testing on multiple api's from restful-booker.herokuapp.com with 100,200,400,600,800,1000,1500,2000,2500 and 3000 threads by applying api chaining and also using data from csv file.
</pre>
 
# Walk-through
<pre>
  1. Used api's from https://restful-booker.herokuapp.com/ and information about api's is in API Testing.pdf file.<br/>
  2. Defined variable.
</pre>


 ![Screenshot 2024-12-20 201227](https://github.com/user-attachments/assets/2ad209c8-8db3-45aa-a10e-1a524a7c7041)
<pre>
 3. Project has 6 HTTP Requests.
</pre>
 ![Screenshot 2024-12-20 201227](https://github.com/user-attachments/assets/9f738d6e-8632-498c-8dc0-3eac3a21bc51)

 <pre>
 4.HTTP requests auth(POST)<br/>
   Taken data from defined variables in body data of create http request.
   Generated token and captured as variable token for update HTTP requests.
 </pre>
 
 ![Screenshot 2024-12-20 201359](https://github.com/user-attachments/assets/ced80fe8-b5d2-4318-ad55-8bb627df1b92)
 <pre>
   JSON Extractor captures token as extractedToken from response
 </pre>
 
![Screenshot 2024-12-20 201329](https://github.com/user-attachments/assets/e20af9c6-0634-4b7a-8361-73660bd03cc6)
<pre>
  Response data
</pre>
![Screenshot 2024-12-20 201425](https://github.com/user-attachments/assets/87d089a0-da6e-4582-b183-18844dd8c7f0)
<pre>
 5.HTTP requests createBooking(POST)<br/>
   Used csv data from data.csv and initialized in CSV Data Set Config file.
</pre>
![Screenshot 2024-12-20 201455](https://github.com/user-attachments/assets/ab755ee3-7b52-4255-b834-9ffadc5a2592)
![data](https://github.com/user-attachments/assets/dc8b4fb1-6634-4e2b-bf28-57298f4a47aa)
<pre>
  Response Code assertion
</pre>
![Screenshot 2024-12-20 201524](https://github.com/user-attachments/assets/5c9819c8-dd53-483e-a2f8-ffbc97c53ef1)
<pre>
  Request and Response Data
</pre>
![requestdata](https://github.com/user-attachments/assets/1b32db72-f5a2-4c57-80e2-a51dd1da58d1)
![responsedata](https://github.com/user-attachments/assets/9824dfda-2fa0-4c82-a8ad-be91959135ac)
<pre>
  JSON Extractor captures bookingid as bookingiIdCreated from response for further operations.
</pre>
![create json extractor](https://github.com/user-attachments/assets/33ab7162-01ac-47fa-a0f5-988c0b67cbb3)

<pre>
  6.HTTP requests getBooking(GET)
    Sample result from get http request as Request and Response Data
</pre>
![Screenshot 2024-12-20 201619](https://github.com/user-attachments/assets/9ca25f38-8e10-4101-a19b-5f129a3bbcd4)
![Screenshot 2024-12-20 201642](https://github.com/user-attachments/assets/a0b8e5a8-192e-4d45-936d-58f7e52e2b6d)

<pre>
  7.HTTP requests updateBooking(PUT)
    Taken data from defined variables in body data of updateBooking http request and used token value
    for authorization
</pre>
![Screenshot 2024-12-20 201718](https://github.com/user-attachments/assets/f2f39148-64b5-4efa-99de-b8ccc594e742)
<pre>
  Request and Response Data
</pre>
![Screenshot 2024-12-20 201751](https://github.com/user-attachments/assets/dd8adadf-de54-4e83-91d0-b6e03a3a0d25)
![Screenshot 2024-12-20 201821](https://github.com/user-attachments/assets/557fb2da-b5b4-4d8f-aba1-0247941c0408)

<pre>
  8.HTTP request updateBookingByPatch
    Only update some variables.
</pre>

![Screenshot 2024-12-20 201847](https://github.com/user-attachments/assets/cc6e6f0a-caf0-4978-afb4-4ae117eff04d)
<pre>
  Request and Response Data
</pre>
![Screenshot 2024-12-20 201913](https://github.com/user-attachments/assets/81e21b38-2dd5-488b-b3f0-467d09d409f9)
![Screenshot 2024-12-20 201935](https://github.com/user-attachments/assets/03787967-b3ea-41ea-9e00-abae4850c22c)

# Result For GUI and CLI(Non-GUI) Mode for different threads
<pre>
  <b>For 100 Threads</b>
</pre>
<pre>
  GUI Mode
</pre>
![Screenshot 2024-12-20 201302](https://github.com/user-attachments/assets/66c43c81-a32e-4601-b4d2-90b054a609ed)
![Screenshot 2024-12-20 202008](https://github.com/user-attachments/assets/31ff66a0-db5d-4b3f-b331-f0c976e38819)
<pre>
  CLI(Non-GUI) Mode
</pre>
![Screenshot 2024-12-25 015300](https://github.com/user-attachments/assets/2342fb99-0172-4a41-a960-44d67565f758)
![Screenshot 2024-12-25 015137](https://github.com/user-attachments/assets/eee70f53-6fb6-4d32-9d8e-e13367e5612e)

<pre>
  <b>For 200 Threads</b>
</pre>
<pre>
  GUI Mode
</pre>
![Screenshot 2024-12-20 201302](https://github.com/user-attachments/assets/66c43c81-a32e-4601-b4d2-90b054a609ed)
![Screenshot 2024-12-20 202008](https://github.com/user-attachments/assets/31ff66a0-db5d-4b3f-b331-f0c976e38819)
<pre>
  CLI(Non-GUI) Mode
</pre>
![Screenshot 2024-12-25 015300](https://github.com/user-attachments/assets/2342fb99-0172-4a41-a960-44d67565f758)
![Screenshot 2024-12-25 015137](https://github.com/user-attachments/assets/eee70f53-6fb6-4d32-9d8e-e13367e5612e)

<pre>
  <b>For 400 Threads</b>
</pre>
<pre>
  GUI Mode
</pre>
![Screenshot 2024-12-20 201302](https://github.com/user-attachments/assets/66c43c81-a32e-4601-b4d2-90b054a609ed)
![Screenshot 2024-12-20 202008](https://github.com/user-attachments/assets/31ff66a0-db5d-4b3f-b331-f0c976e38819)
<pre>
  CLI(Non-GUI) Mode
</pre>
![Screenshot 2024-12-25 015300](https://github.com/user-attachments/assets/2342fb99-0172-4a41-a960-44d67565f758)
![Screenshot 2024-12-25 015137](https://github.com/user-attachments/assets/eee70f53-6fb6-4d32-9d8e-e13367e5612e)

<pre>
  <b>For 600 Threads</b>
</pre>
<pre>
  GUI Mode
</pre>
![Screenshot 2024-12-20 201302](https://github.com/user-attachments/assets/66c43c81-a32e-4601-b4d2-90b054a609ed)
![Screenshot 2024-12-20 202008](https://github.com/user-attachments/assets/31ff66a0-db5d-4b3f-b331-f0c976e38819)
<pre>
  CLI(Non-GUI) Mode
</pre>
![Screenshot 2024-12-25 015300](https://github.com/user-attachments/assets/2342fb99-0172-4a41-a960-44d67565f758)
![Screenshot 2024-12-25 015137](https://github.com/user-attachments/assets/eee70f53-6fb6-4d32-9d8e-e13367e5612e)

<pre>
  <b>For 800 Threads</b>
</pre>
<pre>
  GUI Mode
</pre>
![Screenshot 2024-12-20 201302](https://github.com/user-attachments/assets/66c43c81-a32e-4601-b4d2-90b054a609ed)
![Screenshot 2024-12-20 202008](https://github.com/user-attachments/assets/31ff66a0-db5d-4b3f-b331-f0c976e38819)
<pre>
  CLI(Non-GUI) Mode
</pre>
![Screenshot 2024-12-25 015300](https://github.com/user-attachments/assets/2342fb99-0172-4a41-a960-44d67565f758)
![Screenshot 2024-12-25 015137](https://github.com/user-attachments/assets/eee70f53-6fb6-4d32-9d8e-e13367e5612e)

<pre>
  <b>For 1000 Threads</b>
</pre>
<pre>
  GUI Mode
</pre>
![Screenshot 2024-12-20 201302](https://github.com/user-attachments/assets/66c43c81-a32e-4601-b4d2-90b054a609ed)
![Screenshot 2024-12-20 202008](https://github.com/user-attachments/assets/31ff66a0-db5d-4b3f-b331-f0c976e38819)
<pre>
  CLI(Non-GUI) Mode
</pre>
![Screenshot 2024-12-25 015300](https://github.com/user-attachments/assets/2342fb99-0172-4a41-a960-44d67565f758)
![Screenshot 2024-12-25 015137](https://github.com/user-attachments/assets/eee70f53-6fb6-4d32-9d8e-e13367e5612e)

<pre>
  <b>For 1500 Threads</b>
</pre>
<pre>
  GUI Mode
</pre>
![Screenshot 2024-12-20 201302](https://github.com/user-attachments/assets/66c43c81-a32e-4601-b4d2-90b054a609ed)
![Screenshot 2024-12-20 202008](https://github.com/user-attachments/assets/31ff66a0-db5d-4b3f-b331-f0c976e38819)
<pre>
  CLI(Non-GUI) Mode
</pre>
![Screenshot 2024-12-25 015300](https://github.com/user-attachments/assets/2342fb99-0172-4a41-a960-44d67565f758)
![Screenshot 2024-12-25 015137](https://github.com/user-attachments/assets/eee70f53-6fb6-4d32-9d8e-e13367e5612e)

<pre>
  <b>For 2000 Threads</b>
</pre>
<pre>
  GUI Mode
</pre>
![Screenshot 2024-12-20 201302](https://github.com/user-attachments/assets/66c43c81-a32e-4601-b4d2-90b054a609ed)
![Screenshot 2024-12-20 202008](https://github.com/user-attachments/assets/31ff66a0-db5d-4b3f-b331-f0c976e38819)
<pre>
  CLI(Non-GUI) Mode
</pre>
![Screenshot 2024-12-25 015300](https://github.com/user-attachments/assets/2342fb99-0172-4a41-a960-44d67565f758)
![Screenshot 2024-12-25 015137](https://github.com/user-attachments/assets/eee70f53-6fb6-4d32-9d8e-e13367e5612e)

<pre>
  <b>For 2500 Threads</b>
</pre>
<pre>
  GUI Mode
</pre>
![Screenshot 2024-12-20 201302](https://github.com/user-attachments/assets/66c43c81-a32e-4601-b4d2-90b054a609ed)
![Screenshot 2024-12-20 202008](https://github.com/user-attachments/assets/31ff66a0-db5d-4b3f-b331-f0c976e38819)
<pre>
  CLI(Non-GUI) Mode
</pre>
![Screenshot 2024-12-25 015300](https://github.com/user-attachments/assets/2342fb99-0172-4a41-a960-44d67565f758)
![Screenshot 2024-12-25 015137](https://github.com/user-attachments/assets/eee70f53-6fb6-4d32-9d8e-e13367e5612e)

<pre>
  <b>For 3000 Threads</b>
</pre>
<pre>
  GUI Mode
</pre>
![Screenshot 2024-12-20 201302](https://github.com/user-attachments/assets/66c43c81-a32e-4601-b4d2-90b054a609ed)
![Screenshot 2024-12-20 202008](https://github.com/user-attachments/assets/31ff66a0-db5d-4b3f-b331-f0c976e38819)
<pre>
  CLI(Non-GUI) Mode
</pre>
![Screenshot 2024-12-25 015300](https://github.com/user-attachments/assets/2342fb99-0172-4a41-a960-44d67565f758)
![Screenshot 2024-12-25 015137](https://github.com/user-attachments/assets/eee70f53-6fb6-4d32-9d8e-e13367e5612e)
<pre>
  To run and generate report in CLI Mode for 100 threads run following commands:
</pre>
```bash
      jmeter -n -t project_t100.jmx -l report\project_t100.jtl
```
```bash
      jmeter -g report\project_t100.jtl -o report\project_t100.html
```
