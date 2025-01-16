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
![Screenshot 2024-12-20 202730](https://github.com/user-attachments/assets/bf31b892-b2cf-4627-9462-3c3350d7f1ff)
![Screenshot 2024-12-20 202805](https://github.com/user-attachments/assets/daa2394d-1d3c-43c2-8913-6adc6e3f84a9)

<pre>
  CLI(Non-GUI) Mode
</pre>
![200](https://github.com/user-attachments/assets/35cbe30e-c998-4b6f-b47a-966d392d9496)
![201](https://github.com/user-attachments/assets/fb72ca50-f3b2-4aff-90ad-f3ede938d07c)

<pre>
  <b>For 400 Threads</b>
</pre>
<pre>
  GUI Mode
</pre>
![Screenshot 2024-12-20 203006](https://github.com/user-attachments/assets/0eb0cf8b-71d0-44e6-b828-522cf64ce6d7)
![Screenshot 2024-12-20 203034](https://github.com/user-attachments/assets/f2b7fdcb-1c9f-41a7-ad55-c44f9b0d2aee)

<pre>
  CLI(Non-GUI) Mode
</pre>
![400](https://github.com/user-attachments/assets/e131fd1f-d453-4af6-944b-59eff7883144)
![401](https://github.com/user-attachments/assets/5fa42d75-8990-4001-b8e5-3b40e0f3dc5a)
<pre>
  <b>For 600 Threads</b>
</pre>
<pre>
  GUI Mode
</pre>
![m](https://github.com/user-attachments/assets/454a16e3-1b92-450e-a316-a77b5a71f3a0)
![Screenshot 2024-12-20 203536](https://github.com/user-attachments/assets/18a81bbb-4e7c-40ef-9eae-9e37edbe474e)

<pre>
  CLI(Non-GUI) Mode
</pre>
![600](https://github.com/user-attachments/assets/e4655b6d-f488-4044-916e-6042e53d93b6)
![601](https://github.com/user-attachments/assets/9282c663-d97b-4f95-bae2-111d718f1def)

<pre>
  <b>For 800 Threads</b>
</pre>
<pre>
  GUI Mode
</pre>
![Screenshot 2024-12-20 203240](https://github.com/user-attachments/assets/0d2acb99-aa1b-4e5d-9659-5cdbfce33e7c)
![Screenshot 2024-12-20 203311](https://github.com/user-attachments/assets/e105efc0-0e32-43b2-867c-cd1dbae9f715)

<pre>
  CLI(Non-GUI) Mode
</pre>
![800](https://github.com/user-attachments/assets/4fe9156d-2033-4a22-8af4-93bd81aac7d6)
![801](https://github.com/user-attachments/assets/8e9c462d-9081-4f56-aca4-ca6239012c39)

<pre>
  <b>For 1000 Threads</b>
</pre>
<pre>
  GUI Mode
</pre>
![Screenshot 2024-12-20 203806](https://github.com/user-attachments/assets/2c9c2abd-28c4-4c20-aab9-aaf9d28cf04d)
![Screenshot 2024-12-20 203833](https://github.com/user-attachments/assets/7d04083a-6fdf-499c-bbd5-87b90b422c12)
<pre>
  CLI(Non-GUI) Mode
</pre>
![1000](https://github.com/user-attachments/assets/448d160d-3fa3-49a4-a058-2911877f6a95)
![1001](https://github.com/user-attachments/assets/afccc443-4a1e-4d29-9978-74182f0702e5)
![1002](https://github.com/user-attachments/assets/6bbb98cd-70e5-44c8-afdd-0453402c7df1)

<pre>
  <b>For 1500 Threads</b>
</pre>
<pre>
  GUI Mode
</pre>
![Screenshot 2024-12-20 204158](https://github.com/user-attachments/assets/81e71930-3079-4b13-8b18-fd02a550dc7c)
![Screenshot 2024-12-20 204225](https://github.com/user-attachments/assets/49bede5f-eb6c-442c-a432-d0d539fee5c8)
<pre>
  CLI(Non-GUI) Mode
</pre>
![1500](https://github.com/user-attachments/assets/beae2142-c918-46b8-aca9-08f20a35b4aa)
![1501](https://github.com/user-attachments/assets/f04dd546-9328-43d6-a4b1-18379ba91b64)
![1502](https://github.com/user-attachments/assets/0d91b5fd-5ddd-4e21-81b6-1992d400d3a4)

<pre>
  <b>For 2000 Threads</b>
</pre>
<pre>
  GUI Mode
</pre>
![Screenshot 2024-12-21 030657](https://github.com/user-attachments/assets/e5396d0d-1066-4552-aa71-62dde7f353b9)
![Screenshot 2024-12-21 030722](https://github.com/user-attachments/assets/c175165d-8f94-4060-bf2f-9567863d37c5)
<pre>
  CLI(Non-GUI) Mode
</pre>
![200](https://github.com/user-attachments/assets/6c9da18a-6e16-4d10-8786-0eb50d122e58)
![201](https://github.com/user-attachments/assets/e2c2af80-a4e9-4979-8164-79cbaa606ff0)
![202](https://github.com/user-attachments/assets/153af628-a7bc-4c9e-9ec9-efefd298950a)

<pre>
  <b>For 3000 Threads</b>
</pre>
<pre>
  GUI Mode
</pre>
![Screenshot 2024-12-24 234718](https://github.com/user-attachments/assets/e5fb3c67-5d08-4764-9779-0d55d8066b71)
![Screenshot 2024-12-24 234747](https://github.com/user-attachments/assets/f6e40d42-024c-4e54-80f5-099e7f513801)
<pre>
  CLI(Non-GUI) Mode
</pre>
![3000](https://github.com/user-attachments/assets/ac0d9ed8-36f3-43c5-8ce6-6691ca92f355)
![301](https://github.com/user-attachments/assets/e515b3bd-9b59-47b8-8357-0a4fedd7b052)
![302](https://github.com/user-attachments/assets/6786383b-caaf-4b89-b175-d2e113fba682)
<pre>
  To run and generate report in CLI Mode for 100 threads run following commands:
</pre>
```bash
      jmeter -n -t project_t100.jmx -l report\project_t100.jtl
```
```bash
      jmeter -g report\project_t100.jtl -o report\project_t100.html
```
