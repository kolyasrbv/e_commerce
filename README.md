# e_commerce

**Tasks**
- How many users do we have who made a purchase only once?
- How many orders per month, on average, are not delivered for various reasons (display details by reasons)?
- For each product, determine on which day of the week the product is most often bought.
- How many purchases does each user make on average per week (by months)? Do not forget that there may not be an integer number of weeks within a month. For example, November 2021 has 4.28 weeks. And within the metrics, this must be taken into account.
- Using pandas, conduct a cohort analysis of users. Between January and December, identify the cohort with the highest retention for the 3rd month. 
- Often for qualitative analysis of the audience I use approaches based on segmentation. Using python, build RFM user segmentation to qualitatively evaluate your audience. In clustering, you can choose the following metrics: R - time from the last purchase of the user to the current date, F - the total number of purchases from the user for all time, M - the amount of purchases for all time. Describe in detail how you created the clusters. For each RFM segment, plot the boundaries of the recency, frequency, and monetary metrics to interpret these clusters. An example of such a description: RFM-segment 132 (recency=1, frequency=3, monetary=2) has limits of recency metrics from 130 to 500 days, frequency from 2 to 5 orders per week, monetary from 1780 to 3560 rubles per week.

**Data description**

*olist_customers_datase.csv*
- customer_id — per-custom user ID
- customer_unique_id - unique user ID (analogue of a passport number)
- customer_zip_code_prefix - user's zip code
- customer_city — user delivery city
- customer_state - user's delivery state

*olist_orders_dataset.csv*
- order_id — unique order identifier (receipt number)
- customer_id — per-custom user ID
- order_status — order status
- order_purchase_timestamp — order creation time
- order_approved_at — order payment confirmation time
- order_delivered_carrier_date - time of transferring the order to the logistics service
- order_delivered_customer_date — order delivery time
- order_estimated_delivery_date - estimated delivery date

*olist_order_items_dataset.csv*
- order_id — unique order identifier (receipt number)
- order_item_id - item identifier within one order
- product_id - product id (analogue of a barcode)
- seller_id — id of the product manufacturer
- shipping_limit_date - maximum date of delivery by the seller to transfer the order to the logistics partner
- price — price per item
- freight_value - goods weight

*Unique order statuses in the olist_orders_dataset table:*
- created - created
- approved - confirmed
- invoiced - an invoice has been issued
- processing - in the process of order assembly
- shipped - shipped from the warehouse
- delivered - delivered to the user
- unavailable - unavailable
- canceled - canceled
