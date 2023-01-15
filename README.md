# _Payment Integration_

## _Payment Gateway Integration_
- **_Stripe_**
- **_Paypal_**
- **_Razorpay_**
- **_PayTm_**
- **_Buildesk_**

### _Difference Payment Aggregator and Payment Gateway_

**_Razorpay_** - Payment Gateway

## _Payment Aggregator:_ 
- Most of the things that you see around are **_Payment Aggregators_**
- It provides you an Interface to pay via multiple options like **_Credit Card, UPI, Net Banking_**
- All these people who collects all these things and provide you an interface are called **_Payment Aggregators._**
- Majority of the Payement Aggregator that you see behind the scene they use "Yes Bank"

## _Payment Gateway:_
- The thin lines where the transaction happens
- Usually majority of the payment gateways are banks
- There are some Paymet Gateway which are international and can be used like **_Alipay(used by PayTm)_**

**_Transactions Per Second(TPS):_** Millions of Transactions happens Per Second

- Majority of the ones that we see around are Payment Aggrerators and they handle the Payment Gateway Part
- You have to accquire a bank lisence in order to become a "Payment Gateway"



### _UPI_
- **_Unified Payments Interface:_** It is totally a different thing

## _Brain Tree Workflow_
![bt](https://user-images.githubusercontent.com/91872149/212537292-14f151c7-7582-4d08-b0b1-7db20ae341a5.png)

## _Steps_

**_Step 1:_** Your front-end requests a client token from your server and initializes the client SDK.

**_Step 2:_** Your server generates and sends a client token back to your client using the server SDK.

**_Step 3:_** The customer submits payment information, the client SDK communicates that information to Braintree and returns a payment method nonce.

**_Step 4:_** Your front-end sends the payment method nonce to your server.

**_Step 5:_** Your server code receives the payment method nonce and then uses the server SDK to create a transaction.

**_Nonce:_** It is a Unique Token

## _Client:_ Web Browser, Mobile App

Step 1: As soon as the client request, 
        Request the sever to Generate a token

Step 2: As soon as the client response back,
        you need to store that token

Step 3: Client request with the token and verifies
        the braintree. Once the braintree receives this, it will
        reply with nonce

Step 4: Your front-end sends the payment method nonce to your server

Step 5: Your server code receives the payment method nonce and then uses the server SDK to create a transaction.

## _With perspective of Backend Developer_

_**Only Two Controllers are needed:**_
- Generate a Token
- Pass the nonce, make a braintree request, send it to frontend

