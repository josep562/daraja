# Daraja M-PESA API Integration
This project is an integration of Safaricom's M-PESA API with a PHP application. It allows users to initiate a payment transaction using the M-PESA payment gateway.


**How it works**<br>
The integration involves two PHP scripts: index.php and stk_initiate.php.
 - index.php: This is the front-end part of the application where users input their phone number and the payment amount.
 - stk_initiate.php: This script handles the backend logic. When the user submits the form on index.php, the data is sent to this script.


The script carries out the following steps:

 - Generates a timestamp and password for the transaction. The password is a base64-encoded string of the M-PESA shortcode, passkey, and timestamp.
 - Obtains an access token from the M-PESA API.
 - Constructs the HTTP POST request to the M-PESA API. The request includes the user's phone number, payment amount, and a callback URL.
 - Uses cURL to send the HTTP POST request to the M-PESA API.
 - The API then prompts the user on their phone to enter their M-PESA PIN to authorize the payment.
 - If the PIN is correct, the payment is processed and the user is redirected to the callback URL.
 - The response from the M-PESA API, including a transaction ID and other payment details, is printed by the script.



**Setup**<br>
To run this project locally:

 - Clone the repository to your local machine.
 - Replace the placeholder values in the scripts with your actual M-PESA shortcode, passkey, and other necessary information.
 - Run the project on a local server. You can use tools like XAMPP or WampServer.
 - Open index.php on your web browser, and try making a payment.

**Note:** You need to have a Safaricom Developer account and a Lipa Na M-PESA Online Shortcode to run this project.

