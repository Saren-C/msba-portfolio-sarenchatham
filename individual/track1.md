# Track 1

## What 3–5 source tables would you expect a real company to use for customer churn? For each source, what does one row represent, for example one customer, one month, one event

1. Customer Profile Table - customer name, customer id, account number, sign-up date, demographic data, etc.
    - one row = 1 customer
2. Subscription Table - contract type, monthly fee, payment type, tenure, etc.
    - one row = 1 account
3. Activity Table - data usage, call minutes, long distance call minutes, streaming, add-on service usage, etc.
    - one row = one customer per month

## What keys would you use to connect the data, for example customer_id, account_id, date, etc?

Customer id as a primary key, account number to connect subscription table to customer and activity tables.

## What are two risks and how would you reduce them? Examples of risks are duplicates, missing IDs, using information that only exists after churn happens, and definitions changing over time.

1. Using after-churn information (data leakage)
    - create a cutt-off date for predictions and filter tables so all data is prior to that date
2. Duplicates ids
    - set primary key contraints if working in SQL, use most recent record and drop previous records if appropriate