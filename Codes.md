## Users Level

| Level | User Type     | access code | Access                                                                                      |
| ----- | ------------- | ----------- | ------------------------------------------------------------------------------------------- |
| 0     | Sellers       | 1           | Support Ask, payment req, payment del, add/edit/view products, view sells/orders, analytics |
| 1     | Support Admin | 0           | add/view/edit Support, res of contact form + resole it, verify users,resole payment         |
| 2     | Super Admin   | 2           | payment, ticket, all support access, inventory, orders                                      |

## Items State Codes

| Level | Name               | Order | Info                 |
| ----- | ------------------ | ----- | -------------------- |
| 0     | Created            | 1st   | Cancel ✅, Return ❌ |
| 1     | Accepted           | 2nd   | Cancel ✅, Return ❌ |
| 2     | In-progress        | 3rd   | Cancel ❌, Return ❌ |
| 3     | Completed          | 4th   | Cancel ❌, Return ✅ |
| 4     | Cancelled          | 5th   | Cancel ❌, Return ✅ |
| 5     | RTO-Initiated      | 6th   | Cancel ❌, Return ✅ |
| 6     | RTO-Disposed       | 7th   | Cancel ❌, Return ✅ |
| 7     | RTO-Delivered      | 8th   | Cancel ❌, Return ✅ |
| 8     | Return_Initiated   | 9th   | Cancel ❌, Return ✅ |
| 9     | Return_Approved    | 10th  | Cancel ❌, Return ✅ |
| 10    | Return_Pick_Failed | 11th  | Cancel ❌, Return ✅ |
| 11    | Return_Picked      | 12th  | Cancel ❌, Return ✅ |
| 12    | Return_Delivered   | 13th  | Cancel ❌, Return ✅ |
| 13    | Return_Failed      | 14th  | Cancel ❌, Return ✅ |
| 14    | Return_Rejected    | 15th  | Cancel ❌, Return ✅ |

## Fulfillment states & mapping to order states

- Hyperlocal

| Fulfillment State  | When to assign state      | Order state             |
| ------------------ | ------------------------- | ----------------------- |
| Pending"           | default fulfillment state | "Created" or "Accepted" |
| "Packed"           | packed for shipping       | "In-progress"           |
| "Agent-assigned"   | rider assigned            | "In-progress"           |
| "Order-picked-up"  | order picked up by rider  | "In-progress"           |
| "Out-for-delivery" | Out for delivery          | "In-progress"           |
| "Order-delivered"  | delivered                 | "Completed"             |
| "Cancelled"        | cancelled                 | "Cancelled"             |

- RTO

| Fulfillment State | When to assign state                                    | Order state                                                |
| ----------------- | ------------------------------------------------------- | ---------------------------------------------------------- |
| "RTO-Initiated"   | When RTO has been initiated                             | Order state before RTO initiated                           |
| "RTO-Disposed"    | RTO terminal state when "return to origin" not required | "Cancelled" (if all fulfillments cancelled) or "Completed" |
| "RTO-Delivered"   | RTO terminal state when "return to origin" required     | "Cancelled" (if all fulfillments cancelled) or "Completed" |

## Issue Code

| respondent_action | Code |
| ----------------- | ---- |
| PROCESSING        | 0    |
| CASCADED          | 1    |
| RESOLVED          | 2    |
| NEED-MORE-INFO    | 3    |

## Action Triggered Code

| action_triggered | Code |
| ---------------- | ---- |
| REFUND           | 0    |
| REPLACEMENT      | 1    |
| CANCEL           | 2    |
| NO-ACTION        | 3    |

## Updates Codes

| Fulfillment State | When to assign state    |
| ----------------- | ----------------------- |
| Return_Initiated  | new fulfillment created |
| Return_Approved   | If return is approved   |
| Liquidated        | If return is approved   |
| Return_Rejected   | If return is rejected   |

## Date and Time Codes

| Label | Meaning                                                                                     |
| ----- | ------------------------------------------------------------------------------------------- |
| H     | is the hour designator that follows the value for the number of hours.                      |
| M     | is the minute designator that follows the value for the number of minutes.                  |
| S     | is the second designator that follows the value for the number of seconds.                  |
|       |                                                                                             |
| P     | is the duration designator (for period) placed at the start of the duration representation. |
| Y     | is the year designator that follows the value for the number of years.                      |
| M     | is the month designator that follows the value for the number of months.                    |
| W     | is the week designator that follows the value for the number of weeks.                      |
| D     | is the day designator that follows the value for the number of days.                        |
| T     | is the time designator that precedes the time components of the representation.             |
|       |                                                                                             |
