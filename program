menu = [
    ("Chicken Burger""Burger με κοτόπουλο, bacon, τυρί edam, τομάτα, μαρούλι με μαγιονέζα", 6.50),
    ("Ham Burger""Burger με μπιφτέκι, τυρί, κέτσαπ, μουστάρδα" ,5.50),
    ("Green Burger""Burger με ζουμερό μπιφτέκι, τυρί, φρέσκια τομάτα, μαρούλι, κρεμμύδι, πίκλες, κέτσαπ και dressing sauce", 6.00),
    ("Club Sandwich""Club sandwich με 3 πλούσιες στρώσεις Philadelphia σε φρυγανισμένο ψωμί του τοστ με ζουμερό κοτόπουλο φιλέρο, bacon, τομάτα, μαρούλι και τηγανητές πατάτες",7.00),
    ("Σαλάτα ceasar’s""Δροσερή πράσινη σαλάτα με ζουμερό κοτόπουλου σε βάση μαρουλιού, με καλαμπόκι, κρουτόν, τριμμένο τυρί και vinaigrette ελαιόλαδου",8.00),
    ("Κινόα με Λαχανικά" "Δροσερή σαλάτα με κινόα, κόκκινη πιπεριά, τοματίνια, αγγούρι, δυόσμο, φρέσκο μαϊντανό και sauce λαδολέμονο",7.50)
]      
 
order = []

while True:
    print("Επιλογές:")
    print("==========")
    print("1. Έναρξη Παραγγελίας")
    print("2. Εμφάνιση Παραγγελίας")
    print("3. Αφαίρεση προϊόντος από την παραγγελία")
    print("4. Πληρωμή")
    choice = input("Εισάγετε την επιλογή: ")
    print("")

    if choice == "1":
        while True:
            print("Μενού:")
            for i, item in enumerate(menu):
                print(f"Επιλογή #{i}: {item[0]} - {item[1]} €")

            item_num = input("Εισάγετε τον αριθμό προϊόντος από το μενού: ")
            if not item_num.isdigit() or int(item_num) < 0 or int(item_num) >= len(menu):
                print("Μη έγκυρη επιλογή. Παρακαλώ προσπαθήστε ξανά.")
                continue

            quantity = input("Εισάγετε ποσότητα: ")
            if not quantity.isdigit() or int(quantity) <= 0:
                print("Μη έγκυρη ποσότητα. Παρακαλώ προσπαθήστε ξανά.")
                continue

            item = (menu[int(item_num)][0], menu[int(item_num)][1], int(quantity))
            order.append(item)

            more = input("Επιθυμείτε να εισάγετε άλλο (ν/ο): ")
            if more.lower() == "ν":
                continue
            else:
                break

    elif choice == "2":
            if not order:
                print("Η παραγγελία είναι κενή.")
            else:
                print("Παραγγελία:")
                for i, item in enumerate(order):
                    print(f"Επιλογή #{i}: {item[0]} - {item[1]} € - {item[2]} τεμάχια")
    elif choice == "3":
        if not order:
            print("Η παραγγελία είναι κενή.")
        else:
            while True:
                print("Αφαίρεση Προϊόντος")
                print("================")
                for i, item in enumerate(order):
                    print(f"Επιλογή #{i}: {item[0]} - {item[1]} € - {item[2]} τεμάχια")

                item_num = input("Εισάγετε τον αριθμό προϊόντος που θέλετε να αφαιρέσετε: ")
                if not item_num.isdigit() or int(item_num) < 0 or int(item_num) >= len(order):
                    print("Μη έγκυρη επιλογή. Παρακαλώ προσπαθήστε ξανά.")
                    continue

                order.pop(int(item_num))

                more = input("Επιθυμείτε να αφαιρέσετε άλλο προϊόν (ν/ο): ")
                if more.lower() == "ν":
                    continue
                else:
                    break

    elif choice == "4":
        if not order:
            print("Η παραγγελία είναι κενή.")
        else:
            print("Παραγγελία:")
            total = 0
            for item in order:
                total += item[1] * item[2]
                print(f"Επιλογή: {item[0]} - {item[1]} € - {item[2]} τεμάχια")
            print(f"Σύνολο: {total} €")
            payment_method = input("Πληρωμή σε μετρητά ή με κάρτα; Εισάγετε 'Μ' για μετρητά ή 'Κ' για κάρτα: ")
            if payment_method == 'Μ':
                cash_given = float(input(f"Παρακαλώ εισάγετε το ποσό που δίνετε (σύνολο: {total} €): "))
                while cash_given <= total:
                    cash_given = int(input(f"Μη έγκυρο ποσό. Παρακαλώ εισάγετε το ποσό που δίνετε (σύνολο: {total} €): "))
                change = cash_given - total
                print(f"Ποσό που δόθηκε: {cash_given} €")
                print(f"Ρέστα: {change} €")
                print(f"Σύνολο: {total} €")
                break
            elif payment_method == 'Κ':
                print("Η πληρωμή έγινε με επιτυχία με κάρτα.")
                for item in order:
                    total += item[1] * item[2]
                    print(f"Επιλογή: {item[0]} - {item[1]} € - {item[2]} τεμάχια")
                    print("ευχαριστουμε για την πληρωμη")
                break
            else:
                print("Παρακαλώ επιλέξτε μετρητά (Μ) ή κάρτα (Κ).")
    else:
        print("Μη έγκυρη επιλογή πληρωμής.")

    
