## english version coming ~~soon~~ at some point

# Πράξεις Πινάκων
Το παρόν πρόγραμμα γράφτηκε από την Αικατερίνη Παπαγιαννίτση και τη Μαρία Μηλιούση ως
εργασία του μαθήματος Δομημένος Προγραμματισμός, έτος 2021-2022, 1ο εξάμηνο.
Το πρόγραμμα εκτελεί πράξεις πινάκων και διανυσμάτων:

α. Πίνακες:
 1. Πρόσθεση
 2. Αφαίρεση
 3. Πολλαπλασιασμός με αριθμό ή πίνακα
 4. Ορίζουσα
 5. Αντίστροφος
 6. Ανάστροφος
 7. Δυνάμεις Πινάκων
 8. Ίχνος
 
β. Διανύσματα:
 1. Πρόσθεση
 2. Αφαίρεση
 3. Εσωτερικό Γινόμενο
 4. Εξωτερικό Γινόμενο

## Πίνακας Περιεχομένων
#### 1. Οδηγίες
#### 2. Περιγραφή
#### 3. Πηγές

## Οδηγίες
• Για την ανάπτυξη του προγράμματος χρησιμοποιήθηκε το ολοκληρωμένο περιβάλον
ανάπτυξης Code::Blocks.

• Για τη μεταγλώττιση του προγράμματος χρειάζονται τα αρχεία: main.c, prakseis.c και
prakseis.h.

• Από τα παραπάνω δημιουργείται το εκτελέσιμο αρχείο main.exe

• Το πρόγραμμα έχει δοκιμαστεί σε Windows 10, ωστόσο ο κώδικας μπορεί να εκτελεστεί και
σε άλλα λειτουργικά συστήματα με ελάχιστες ή και καθόλου αλλαγές

• Το πρόγραμμα λειτουργεί με διαδραστικά μενού: ο χρήστης μπορεί να διαλέξει μία επιλογή
γράφοντας τον αριθμό πληκτρολογώντας τον αριθμό που αντιστοιχεί σε αυτή και πατώντας
το πλήκτρο ENTER. Για παράδειγμα:

![image](https://user-images.githubusercontent.com/97043061/151154034-ba978845-a067-487b-93fe-71aba6198784.png)

![image](https://user-images.githubusercontent.com/97043061/151154416-2dedf359-22cf-4ed5-9685-eef3210f599e.png)

 > Σημείωση: Για προβολή διαθέσιμων συστοιχιών ή επιλογή από διαθέσιμες συστοιχίες χρειάζεται πρώτα δημιουργία ή φόρτωση συστοιχιών

## Περιγραφή
Γενικό σχεδιάγραμμα ροής εκτέλεσης του προγράμματος:
![Untitled Diagram drawio7](https://user-images.githubusercontent.com/97043061/151209147-d642ab27-a047-4a2f-9aed-9f561712bb98.png)

##### Αρχείο main.c:
το αρχείο περιέχει τη main και όλες τις συναρτήσεις που χρησιμοποιούνται εκτός από αυτές
για τις πράξεις πινάκων και διανυσμάτων.

matrix getmatrix():
Εισαγωγή πίνακα από χρήστη.
Εισαγωγή των διαστάσεων της συστοιχίας (με έλεγχο ορίων των διαστάσεων) και εισαγωγή
των στοιχείων τους

save_matrix():
Αποθήκευση Πίνακα σε αρχείο.
Εισαγωγή αναγνωριστικού από τον χρήστη και έλεγχος αν είχε χρησιμοποιηθεί ξανά.
Καταγραφή αναγνωριστικού στις διαθέσιμες συστοιχίες. Δημιουργία αρχείου συστοιχίας και
συμπλήρωση διαστάσεων και τιμών.

show_matrixes():
Προβολή διαθέσιμων πινάκων.
Άνοιγμα αρχείου διαθέσιμων πινάκων και προβολή των αναγνωριστικών πινάκων

load_matrix():
Φόρτωση πίνακα.
Εισαγωγή αναγνωριστικού συστοιχίας απο το χρήστη και συμπλήρωση αναγνωριστικού
συστοιχίας στο αρχείο διαθέσιμων συστοιχιών.

menu():
Προβολή μενού.
Προβολή επιλογών και εισαγωγή αριθμού επιλογής από το χρήστη.

print_elements():
Προβολή στοιχείων συστοιχίας από αρχείο. Εισαγωγή αναγνωριστικού συστοιχίας από τον
χρήστη, άνοιγμα αρχείου συστοιχίας και προβολή στοιχείων.

delete_matrixName():
Διαγραφή αναγνωριστικού.
Μεταφορά όλων των αποθηκευμένων αναγνωριστικών σε νέο αρχείο, έκτος από το
αναγνωριστικό που πρόκειται να διαγραφτεί. Διαγραφή αρχικού αρχείου και μετονομασία του
2ου σε "available_matrix.txt".

delete_matrix():
Διαγραφή συστοιχίας.
Εισαγωγή αναγνωριστικού συστοιχίας για διαγραφή από το χρήστη. Διαγραφή
αναγνωριστικού και διαγραφή αρχείου συστοιχίας.

choose_matrix():
Επιλογή συστοιχίας.
Επιλογή χρήστη αν επιθυμεί να χρησιμοποιήσει μία ήδη υπάρχουσα συστοιχία. ή να εισάγει
μία εκείνη τη στιγμή.

matrix_operations():
Πράξεις πινάκων.
Κάλεσμα συναρτήσεων για πράξεις πινάκων. Αν η πράξη δεν έχει αποτέλεσμα πίνακα, γίνεται
προβολή αποτελέσματος και ο πίνακας αποτελέσματος γίνεται invalid.

vector_operations():
Πράξεις διανυσμάτων.
Κάλεσμα συναρτήσεων για πράξεις πινάκων. Αν η πράξη δεν έχει αποτέλεσμα πίνακα, γίνεται
προβολή αποτελέσματος και ο πίνακας αποτελέσματος γίνεται invalid.

print_matrix():
Προβολή στοιχείων συστοιχίας.

define_matrix():
Αρχικοποίηση συστοιχίας.
Αρχικοποίηση μεταβλητών μέσα στο structure matrix.

startMsg():
Προβολή αρχικού μηνύματος.
Προβολή ονομάτων των δημιουργών του προγράμματος.


##### Αρχείο prakseis.c:
το αρχείο περιέχει τις συναρτήσεις που χρησιμοποιούνται για τις πράξεις πινάκων και
διανυσμάτων.

adj():
Υπολογισμός προσαρτημένου πίνακα.
inverse_matrix():
Υπολογισμός αντίστροφου πίνακα. Έλεγχος αν ο πίνακας που δώθηκε είναι αντιστρέψιμος.

exp_matrix():
Δυνάμεις πινάκων.
Πολλαπλασιασμός τετραγωνικού πίνακα με τον εαυτό του ν φορές.

ixnos():
Ίχνος πίνακα.
Έλεγχος αν ο πίνακας είναι τετραγωνικός. Πρόσθεση στοιχείων της κύριας διαγωνίου.

esgin():
Εσωτερικό γινόμενο.
Έλεγχος αν τα διανύσματα έχουν τις ίδιες διαστάσεις. Υπολογισμός εσωτερικού γινομένου
δύο διανυσμάτων Α και Β.

transpose_matrix():
Υπολογισμός ανάστροφος ενός πίνακα.
Αναστροφή γραμμών και στηλών.

multiplication_matrix():
Πολλαπλασιασμός 2 πινάκων.
Έλεγχος αν ορίζεται ο πολλαπλασιασμός.

subtraction_matrix():
Αφαίρεση 2 πινάκων.
Έλεγχος αν ορίζεται η αφαίρεση.

sum_matrix():
Πρόσθεση 2 πινάκων.
Έλεγχος αν ορίζεται η πρόσθεση.

det():
Yπολογισμός ορίζουσας.

cofactor():
Συμπαράγοντας Αxy.

vector_product():
Eξωτερικό γινόμενο.
Έλεγχος ότι τα διανύσματα ανήκουν στον Διανυσματικό Χώρο R^3.

multiply_byNumber():
Πολλαπλασιασμός πίνακα με αριθμό.
Πολλαπλασιασμός κάθε στοιχείου του πίνακα με σταθερό αριθμό.

##### Αρχείο prakseis.h:
το αρχείο περιέχει τα declarations για το αρχείο prakseis.c

## Πηγές
* Διαφάνειες του μαθήματος Δομημένος Προγραμματισμός 1ου εξαμήνου Ηλεκτρολόγων Μηχανικών και Μηχανικών Υπολογιστών ΑΠΘ
* Η Γλώσσα C Σε Βάθος - Νίκος Χατζηγιαννάκης
* https://www.tutorialspoint.com/cprogramming/c_return_arrays_from_function.htm
