**Απομακρυσμένη Ζυγαριά μελισσιού - Beescale**
===============================================

##Σύντομη Περιγραφή
===================

O μικροεπεξεργαστής Arduino ειναι μια ανοιχτού-κώδικα πλατφόρμα πρωτοτυποποίσης, βασισμένη σε ένα εύχρηστο λογισμικό(software) και υλισμικό(hardware). Ο Arduino έχει την ικανότητα να δέχεται εισόδους -το φώς σε εναν αισθητήρα, το δάχτυλο σε ενα διακόπτη, ή ενα μήνυμα στο Twitter - και να το μετατρέπει σε μια έξοδο - να ενεργοποιήσουν εναν κινητήρα, να ανάψουν ενα LED, να δημοσιεύσει κατι στο ίντερνετ. Όλα αυτά καθορίζονται απο ένα σετ οδηγιών που έχουν προγραμματιστεί μέσω του λογισμικού του Arduino (IDE).

Αν δεν έχετε προηγούμενη εμπειρία με τον Arduino ή άλλον μικροεπεξεργαστή και κυκλώματα, θα ήταν προτιμότερο να δείτε απλούστερα παραδείγματα πριν επιχειρήσετε να φτιάξετε μόνοι σας την ζυγαριά.

Για το εγχείρημα της ζυγαριάς του μελισσιού (beescale) θα χρησιμοποιήσουμε τον Arduino Uno, εναν αισθητήρα θερμοκρασίας, εναν αισθητήρα υγρασίας, έναν αισθητήρα μέτρησης βάρους και ενα πρόσθετο gsm shield ωστε να λαμβάνουμε τις μετρήσεις μεσω δικτύου κινητής τηλεφωνίας. Για την μέτρηση του βάρους απαιτείται η ενίσχυση του σήματος του αισθητήρα βάρους, οπότε θα χρησιμοποιήσουμε και ένα τυπωμένο κύκλωμα σε πλακέτα (printed circuit board - PCB) με τον HX711 ενισχυτή σήματος.


* __Μικροεπεξεργαστής: Arduino Uno__
* __Αισθητήρας Θερμοκρασίας: Dallas DS18B20__
* __Αισθητήρας Υγρασίας: DHT11__
* __Αισθητήρας μέτρησης βάρους: Load cell 100 kg__
* __Ενισχυτής σήματος: DFRobot HX711__
* __Πρόσθετο PCB για σύνδεση στο δίκτυο κινητής τηλεφωνίας: Adafruit Gsm Shield__ 
* __Κεραία για το gsm shield: Mini GSM/Cellular Quad-Band Antenna - 2dBi SMA Plug__


Πιο συγκεκριμένα, oποιαδήποτε στιγμή ο μελισσοκόμος θέλει να ενημερωθεί για τις συνθήκες που επικρατούν στην κυψέλη του, θα λαμβάνει ένα μήνυμα στο κινητό του τηλέφωνο με τις τρέχουσες μετρήσεις της ζυγαριάς, η οποία θα τίθεται αυτόματα σε λειτουργία, καθώς και τις ενδείξεις των αισθητήρων. Επιπροσθέτως, ο μικροεπεξεργαστής θα δημιουργεί ένα αρχείο μετρήσεων, έτσι ώστε να είναι δυνατή η περαίτερω επεξεργασία τους με σκοπό την μακροπρόθεσμη εξαγωγή συμπερασμάτων για τη βελτίωση της παραγωγής.

Σε ποίους απευθύνεται
==========================
##Κοινότητες Χρηστών

Το beescale απευθύνεται σε όλους όσους ασχολούνται με την μελισσοκομία, επαγγελματίες ή μη μελισσοκόμους δηλαδή, οι οποίοι θέλουν να γλιτώσουν χρόνο και χρήμα από τις μετακινήσεις τους την περίοδο του τρύγου του μελιού.

##Κοινότητες προγραμματιστών

Προγραμματιστές που ενδιαφέρονται για την επέκταση του έργου μπορούν να συμβάλουν ώστε το beescale να ενισχυθεί με gps σύστημα με σκοπό την μεγαλύτερη ασφάλεια των κυψελών  από κλοπές.


##Κόστος 


|Κόστος 																		||
|---------------|----------|--------------------------------------------------------------------------------------------|
|Mικροεπεξεργαστή Arduino uno|                                   €24.60|
|Arduino gsm shield     |                                        €80.0|
|Kεραία SMA         |                                          €4.00|
|Aισθητήρα βάρους (load cell)      |                             €10.00|
|Eνισχυτή σήματος HX711      |                                   €18,60|
|Aισθητήρα θερμοκρασίας Dallas DS1820   |                        €2.00|
|Aισθητήρα υγρασίας DHT11          |                             €3.00|
|Διαφορα Ηλεκτρονικα εξαρτήματα (καλωδια, αντιστασεις,pins.. )|  €5.00|
|Ξύλα          |                                                 €10.00|
|**Σύνολο**        |                                                 €157.2 |


Στη σελίδα του [Wiki](https://github.com/ellak-monades-aristeias/beescale/wiki/) υπάρχει οδηγός που αναλύει βήμα προς βήμα πως μπορείτε να κατασκευάσετε ένα πρωτότυπο beescale.


|Πίνακας Παραδοτέων||
|-------------------------------------------------|----------------------------------------------------|
|Παραδοτέο|	URL|
|Πηγαίος Κώδικας υλοποίησης της πρότασης έργου|	https://github.com/ellak-monades-aristeias/beescale/tree/master/Code|
|Συνδεσμολογία των κυκλωμάτων του συστήματος με γραφήματα|https://github.com/ellak-monades-aristeias/beescale/tree/master/Hardware|
|Αναλυτικός οδηγός κατασκευής|	https://github.com/ellak-monades-aristeias/beescale/wiki/%CE%9A%CE%B1%CF%84%CE%B1%CF%83%CE%BA%CE%B5%CF%8D%CE%B1%CF%83%CE%B5%20%CF%84%CE%BF%20%CE%B4%CE%B9%CE%BA%CF%8C%20%CF%83%CE%BF%CF%85%20beescale|



##English description of Beescale

The beekeeper wants to be informed about the weight of his hives, that means about how much honey there is inside the beehive. The beescale is set to send an SMS periodically to the beekeeper (once a day or more) including the kilograms the temperature and the humidity of the hive.

So he can :

  * __know if the nectar flow is over and he should go to pick up the honey so he can save lot ot fuels__
  * __know if the bees needs to be feeding at winter time__
  * __compare colony strength and productivity by seeing which colonies are most productive throughout the season__
  * __know the weather conditions of the area__

In conclusion, depending on the message, he can take the best decision about his actions

You can see full details and tutorials at our [English Wiki](https://github.com/ellak-monades-aristeias/beescale/wiki)
