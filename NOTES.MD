- In this function "def dates_overlap" the problem is when a user books from Jan 8 - Jan 20, it will still proceed because of this code
    "return start_b <= start_a <= end_b" this condition only checks if the start date of the new booking is within the existing booked dates so i changed it to "return start_a <= end_b and end_a >= start_b" this checks both the start and end dates of the new booking, if both conditions are "True" the booking will not be accepted

- In this function "def rental_days" the problem is when you book from Jan 10 - Jan 15, it only calculates 5 days instead of 6 days because the end date is not included, i fixed it by adding +1

- In this function "def create_booking" i added a condition to prevent users from booking equipment that is under maintenance, if the equipment status is "maintenance", it returns a 400 error.
    if equipment["status"] == "maintenance":
        return jsonify({"error": "Equipment under maintenance"}), 400

- In index.html there was a missing event listener for the end date input, because of this, changing the end date did not update the total price, i add by adding an event listener to call updateTotal() whenever the end date changes


- I used ChatGPT to help me complete the code because im not good at memorizing code, functions, and conditions. I first read the task, found the related function, and tested the bug. Then I copied that function into ChatGPT and explained the issue. After applying the suggested fix, i tested and debugged it to make sure the output matched the expected result
