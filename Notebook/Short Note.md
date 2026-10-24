## Short note for the 4th Question
4.

a. customer_id is generated for each order, so it is unique in customers (99,441 distinct in 99,441 rows). customer_unique_id identifies the person and repeats when someone orders again (96,096 distinct, with one person holding up to 17 customer_id values). Count customers with customer_unique_id.

b. order_items is the junction table. Its composite key is (order_id, order_item_id), and it resolves the many-to-many relationships between orders and products and between orders and sellers (and so indirectly between products and sellers).

c. The data is stricter than the diagram for products to order_items: every product has at least one sale (min = 1, max = 527), but the diagram keeps the circle because a catalogue product may not have sold yet. The circle on orders to order_items is justified by the data: 775 orders have no items (min = 0), mostly unavailable and canceled orders.