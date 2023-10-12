# Task-Restaurant---Order-Food-
To implement a program that manages food orders in a student dormitory
restaurant located inside the campus of our University. This program will
is available to the waiter where he will note which table each one is at
order, the products of the order and will calculate the final price. As an extra
question you can also implement the payment by card or cash. In case
that the user chooses cash payment should be properly checked if
the waiter needs to give change.
More specifically, the available products will be in a list where each list
contains 4 elements (product name, description, price). In detail it will have:
menu = [
(“Chicken Burger”, “Burger with chicken, bacon, edam cheese, tomato, lettuce with
mayonnaise”, 4.20 ),
("Ham Burger", "Burger with burger, cheese, ketchup, mustard", 2.85),
(“Green Burger”, “Burger with juicy burger, cheese, fresh tomato, lettuce,
onion, pickles, ketchup and dressing sauce”, 4.20),
(“Club Sandwich”, “Club sandwich with 3 rich layers of Philadelphia in
toasted bread with juicy chicken fillet, bacon, tomato,
lettuce and fries”, 10.90),
(“Ceasar's salad”, “Cool green salad with juicy chicken base
lettuce, with corn, croutons, grated cheese and olive oil vinaigrette",
6.90),
("Quinoa with Vegetables", "Cool salad with quinoa, red pepper, cherry tomatoes,
cucumber, mint, fresh parsley and olive oil sauce.", 6.30)
]
You need to implement an order handler with a list, containing in order
of, tuples of two elements each, with the position of the product selected by the
list from the menu and the corresponding quantity for each product.
