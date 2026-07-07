- In this function "def dates_overlap" the problem is when a user books from Jan 8 - Jan 20, it will still proceed because of this code
    "return start_b <= start_a <= end_b" this condition only checks if the start date of the new booking is within the existing booked dates so i changed it to "return start_a <= end_b and end_a >= start_b" this checks both the start and end dates of the new booking, if both conditions are "True" the booking will not be accepted

  <img width="427" height="327" alt="image" src="https://github.com/user-attachments/assets/05c2a8fa-62ad-4c4c-8c9c-4078d71642be" /><img width="437" height="337" alt="image" src="https://github.com/user-attachments/assets/811e82ea-6947-4daa-ad9e-3d09db1f79fc" />


- In this function "def rental_days" the problem is when you book from Jan 10 - Jan 15, it only calculates 5 days instead of 6 days because the end date is not included, i fixed it by adding +1

 <img width="417" height="323" alt="image" src="https://github.com/user-attachments/assets/665a568b-387e-4946-8f97-f1701dd90bc3" /><img width="445" height="347" alt="image" src="https://github.com/user-attachments/assets/06506a37-3d4a-48f3-ba0a-93aa9aff200d" />



- In this function "def create_booking" i added a condition to prevent users from booking equipment that is under maintenance, if the equipment status is "maintenance", it returns 400 cannot process request of user
  
  <img width="401" height="350" alt="image" src="https://github.com/user-attachments/assets/4dc299b7-943b-4908-9c98-5416f98c6ccb" /><img width="408" height="351" alt="image" src="https://github.com/user-attachments/assets/091c47f2-6aa1-44ec-a4dd-eceb786892ec" />



- In index.html there was a missing event listener for the end date input, because of this, changing the end date did not update the total price, i add by adding an event listener to call updateTotal() whenever the end date changes, even tho not clicking the "Create Booking" button it will change the total price

   <img width="427" height="370" alt="image" src="https://github.com/user-attachments/assets/cc4c2cd0-79e9-489a-87f7-2d0b5da879c5" /><img width="421" height="345" alt="image" src="https://github.com/user-attachments/assets/069670cd-f012-4168-a88d-f556af20a8d3" />




- I used ChatGPT to help me complete the code because im not good at memorizing code, functions, and conditions. I first read the task, found the related function, and tested the bug. Then I copied that function into ChatGPT and explained the issue. After applying the suggested fix, i tested and debugged it to make sure the output matched the expected result
