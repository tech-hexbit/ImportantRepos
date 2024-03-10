# Pending

## Website

- issue flow
- send email when the ticket is rasised and recived a reply, etc.
- OTP (system)
- Payment GateWay
- System Generated Emails - In the footer of the emails required
- Fulfillment state update flow
- RTO state flow update

### Saved Data

- Item
  - store item imported_product_country_of_origin
- Store
  - long_desc
  - short_desc
  - category

## ONDC

- taxes value (for each sub Category)
- breakUps

### search

- add domain filter
- long_desc, short_desc save to show data
- locality, street, building, and c/o save to show data

### select

### init

- availability in stock > 0 ✅
- lock the stock

### confirm

### cancel

- RTO state flow update

### status

- Fulfillment state update

### update

- update breakup
- partial cancel
- update the return status
- send mail on order return Initiated or return status is changed

## Security

| Website            | ONDC                       |
| ------------------ | -------------------------- |
| network encryption | apply ttl                  |
| CSRF               | incomming sign verfication |
