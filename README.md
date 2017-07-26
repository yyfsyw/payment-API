# payment-API
a website to work on credit card payment 
Introduction:

The third party payment API I used is Stripe. How it works?
    1. When webpage load, stripe-payment.js file, which I wrote, will create the secure card input fields for user to type in their card.
    Meanwhile, it also do error checking.
    
    2. When user finish filling in form and click confirm button, the Server will charge certain money for the card and send out message
    
    3. if success, redirect to successful page; otherwise, show error messages.
    
By going  through the whole process, server cannot get any information of Card Credentials. the
only thing the  server obtain is a token from Stripe, which is used for charging money, and more usages.
Security is guaranteed.

Notice:

In real business, all transactions should be under HTTPS protocol. (I did testing under HTTP)

My Stripe Account monitor all activities such as creating token, making charges, failure notification, etc.


How to use:

    1. Place the payment folder under your 'localhost' folder or Server.
        1. For mac users, more details how to set up localhost on this site: 
           https://coolestguidesontheplanet.com/get-apache-mysql-php-and-phpmyadmin-working-on-osx-10-11-el-capitan/
        2. For windows users, more details how to set up localhost on this Video:
           https://www.youtube.com/watch?v=6LjpyHoXVjo

    
    2. open the step-1.html to begin.
    
    3. Please Don't use real Credit Card or Debit Card to do Testing!!!!! This is only 
       under test mondel in Stripe. The real card will cause issues and not secure for yourself.
       
      Using the following card Number to test:

      
    4242424242424242	Visa
    4012888888881881	Visa
    4000056655665556	Visa (debit)
    5555555555554444	Mastercard
    5200828282828210	Mastercard (debit)
    5105105105105100	Mastercard (prepaid)
    378282246310005	    American Express
    371449635398431	    American Express
    6011111111111117	Discover
    6011000990139424	Discover
    30569309025904	    Diners Club
    38520000023237	    Diners Club
    3530111333300000	JCB
    3566002020360505	JCB

      All the other information such as expiration date, CVC and zipcode are free to choose.
    
    4. Session variables $_SESSION['pay-process'] is used for purpose, which enforcing user from 
       very first step going through the final step.
       
    5. When payment succeed, you will only have 10 min to send out message. Otherwise, You won't 
       get any information from email even through you will still get email. 

    6. image upload is not fully working; however it won't affect the whole workflow. It's kind of
       hard to deal with files using php. I didn't want to put so much time on it.
    
    7. In the step-2 page, I cannot change the CC detail of Billing summary section because we 
       just typed in the card number, it’s impossible to show encrypted card info without clicking the Button.








