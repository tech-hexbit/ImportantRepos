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
  - save data for address = street, Pin code, State, City, Building

## ONDC

- taxes value (for each sub Category)
- created_at, updated_at fix.
- Delivery charges, Convenience Fee to be added once and dynamic
- breakUps
- prices flow

### search

- add domain filter
- long_desc, short_desc save to show data
- locality, street, building, and c/o save to show data

### select

- provider ID in select for Logistics

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

## Hexbit Backend

- make 2 servers (1 ONDC | 1 Backend)
- make the seller connected to bank, kyc (bidirectional graph)

## Security

| Website            | Datails |
| ------------------ | ------- |
| network encryption |         |
| CSRF               |         |

| ONDC                       |     |
| -------------------------- | --- |
| apply ttl                  |     |
| incomming sign verfication |     |
