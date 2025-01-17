# Marketplace-Technical-Foundation

day 2 of 7 day hackathhone

##API End point
/Proucts-------> GET --------> fetchProducts
/Order------>POST----------> OrderDetail
/Checkout-------> POST----------> Postdetail

### Architecture
+-------------------+
|       User        |
+-------------------+
  |
  V
+-------------------+
|     Frontend      |
+-------------------+
  |           |
  V           V
+-------------------+  +-------------------+
|      Sanity      |  |      Auth       |
+-------------------+  +-------------------+
  |           |
  V           V
+-------+  +-------+  +-------------------+
| Store |  | Manage |  |  Handles  |
+-------+  +-------+  +-------------------+
  |       |       |       |
  V       V       V       V
+-------+  +-------+  +-------+  +-------+
|Product|  | Orders|  | Content|  | Customer|
+-------+  +-------+  +-------+  +-------+
  |
  V
+-------------------+
| Third Party APIs |
+-------------------+
  |           |
  V           V
+-------+  +-------+
|Payment|  |Shipment|
+-------+  +-------+

### EXPLANATION :

 * The top level is the "User" who interacts with the "Frontend."
 * The "Frontend" interacts with "Sanity" and "Auth."
 * "Sanity" handles "Store" and "Manage."
 * "Store" is further broken down into "Product."
 * "Manage" is further broken down into "Orders."
 * "Handles" interacts with "Content" and "Customer."
 * The bottom level includes "Third Party APIs" which are further broken down into "Payment" and "Shipment."
