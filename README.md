# StripeTestingFramework
Test automation framework to test payments Stripe API

TEST CASES
Test creating a new customer:

Send a request to the /v1/customers endpoint with the necessary parameters (e.g., name, email).
Verify that the response code is 200 (OK).
Validate that the response contains the expected customer details.
Optionally, clean up the created customer by deleting it after the test.
Test retrieving customer details:

Create a customer using the /v1/customers endpoint.
Send a request to the /v1/customers/{customer_id} endpoint, providing the customer ID obtained from the previous step.
Ensure that the response code is 200 (OK).
Validate that the retrieved customer details match the expected values.
Test creating a payment intent:

Send a request to the /v1/payment_intents endpoint, specifying the necessary parameters (e.g., amount, currency).
Check that the response code is 200 (OK) or 201 (Created).
Validate that the response contains a valid payment intent ID and other relevant details.
Optionally, clean up the created payment intent by canceling or deleting it after the test.
Test processing a payment:

Create a payment intent using the /v1/payment_intents endpoint.
Simulate a payment by sending the necessary details (e.g., card information) to the /v1/payment_intents/{payment_intent_id}/confirm endpoint.
Verify that the response code indicates successful payment processing (e.g., 200 or 201).
Validate that the payment intent status is updated accordingly.
Test creating and managing subscriptions:

Send a request to the /v1/subscriptions endpoint to create a new subscription.
Check that the response code is 200 (OK) or 201 (Created).
Validate that the response contains the expected subscription details.
Perform additional tests to manage the subscription, such as updating the subscription, canceling it, or retrieving subscription details.
Test handling webhook events:

Simulate a webhook event by sending a request to the webhook endpoint specified in your Stripe account settings.
Verify that the response code indicates successful processing (e.g., 200 or 204).
Validate that the webhook event is correctly processed and triggers the expected actions in your system.
