# sw-FINAL_REPORT
#### ΤΕΛΙΚΗ ΑΝΑΦΟΡΑ ΤΕΧΝΟΛΟΓΙΑ ΛΟΓΙΣΜΙΚΟΥ
#### ΑΝΤΡΕΑΣ ΠΑΠΠΟΥΤΑΣ
#### Π2017148


#### [Λινκ εργασίας](https://github.com/andreaspappoutas/sw/tree/2017148/projects/2017148 'Λινκ εργασίας')

#### [Λινκ κλαδί εργασίας](https://github.com/andreaspappoutas/sw/tree/2017148 'Λινκ αποθετηρίου εργασίας')

#### [Προφίλ στο github](https://github.com/andreaspappoutas 'Προφίλ στο github')

#### [Λινκ αποθετηριου τελικης αναφοράς](https://github.com/andreaspappoutas/sw-FINAL_REPORT/ 'Λινκ αποθετηριου τελικης αναφοράς')

## Σύνοψη:
Στο μάθημα πολυμέσα στάλθηκαν 8 παραδοτέα συνολικά όλα στις σωστές προθεσμίες. Στο πρώτο παραδοτέο έγινε χρήση πολλών τέρμιναλ. Στο δεύτερο χρησιμοποίησα το Docker για να ανεβάσω το cv μου σε σελίδα. Στο τρίτο έφτιαξα cloud μέσο του raspberry pi και OpenSSH. Στο τέταρτο παραδοτέο έκανα εγκατάσταση προγράμματος στο ubuntu για ειδοποιήσεις. Στο πέμπτο έγινε "performance monitoring" μέσο hyperfine. Στο παραδοτέο 6 μέσο του travis ci έκανα συνεχής build. Στο παραδοτέο 7 έκανα σύστημα για δημιουργία python προγραμμάτων μέσα σε φάκελο. Στο τελευταίο παραδοτέο χρησιμοποίησα NeoVim και SpaceVim για τη επεξεργασία κώδικα python.

## Σύντομη Εισαγωγή:
Στο πρώτο παραδοτέο κατέβασα και εγκατέστησα τα τερμιναλ guake,konsole,tilda,terminology,yakuake,fish και zsh. Μετά στο δεύτερο παραδοτέο έκανα χρήση του Nginx και Alpine για τη δημιουργία του docker της σελίδας. Για το τρίτο παραδοτέο ενεργοποίησα το OpenSSH στο Raspberry Pi για τη σύνδεση των 2 συστημάτων. Για το τέταρτο παραδοτέο εγκατέστησα το ntfy. Μέσα στο πεμτπο παραδοτέο χρησιμοποίησα το hyperfine. Στη συνεχεία στο έκτο παραδοτέο έκανα χρήση travis ci και github pages. Ακολούθως στο παραδοτέο 7 εγκατέστησα το pipenv και virtualenv. Για τη διεκπεραίωση του τελικού παραδοτέου που έφτιαξα έγινε χρήση του SpaceVim και NeoVim.

## Σύντομη Ανάλυση σχετικών Έργων και Εργαλείων:
Η περάτωση των πιο πάνω εργασιών έγινε μέσα σε τέρμιναλ του Linux. Για τη εγκατάσταση του Linux κατέβασα το λογισμικό του ubuntu και στη συνεχεία χρησιμοποιούσα τη εφαρμογή VirtualBox για να το τρέξω. Με τη εντολή "sudo gedit ~/.bashrc" τροποποίησα το αρχέιο και άλλαξα το όνομα που εμφανίζεται μέσα στο τέρμιναλ. Επίσης εγκατέστησα και έφτιαξα λογαριασμό για τη εφαρμογή asciinema με το οποία έδειξα το κάθε παραδοτέο. Τέλος χρειάστηκα επίσης να χρησιμοποιήσω το Raspberry Pi 3 Model B+.

## Μέθοδος και Τεχνικές Ανάπτυξης:
Αρχικά στο πρώτο παραδοτέο με τα τερμιναλ πρόσεξα ότι δεν φαίνονταν οι αλλαγές του καθενός τερμιναλ μέσο του asciinema, έτσι αποφάσισα να βγάλω εκτός από τα asciinema και gif έτσι ώστε να φανούν καλύτερα μεταξύ τους οι διαφορές. Τα περισσότερα από τα τερμιναλ που δοκίμασα είναι παρόμοια μεταξύ τους εφόσον οι παραπάνω διαφορές είναι εμφανισιακά αλλά 2 τέρμιναλ φάνηκαν καλύτερα από τα άλλα το zsh και fish. Το zsh είναι ανοικτού κώδικα και προσφέρει 275 plugins ειδικά για προγραμματιστές. Το fish shell προσφέρει αυτόματη συμπλήρωση και πολλές δικές του εντολές. Στο δεύτερο παραδοτέο δημιούργησα docker image με Nginx και Alpine για να δημιουργήσω σελίδα με το CV μου . Πρώτα απ όλα εφόσον είχα το ngix πάνω στο υπολογιστή μπήκα στο φάκελο του (/usr/share/nginx/html) και έβαλα το index.html του CV μου. Στη συνέχεια δημιούργησα και τροποποίησα το DockerFile μου έτσι ώστε να τρέχει το ngix με το CV μου μέσα στο alpine (FROM nginx:alpine COPY index.html /usr/share/nginx/html). Στη συνέχεια έτρεξα τη εντολή για να δημιουργηθεί το docker image(sudo docker build -t html-server-image:v1 .) και τη τρέχω σε port 80 για να εμφανιστή στο localhost (sudo docker run -d -p 80:80 html-server-image:v1). Στο παραδοτέο 3 έκανα χρήση του Raspberry Pi μαζί με OpenSSH. Στη αρχή έκανα εγκατάσταση του OpenSSH πάνω στο σύστημα ubuntu (sudo apt-get install openssh-server) και στο Raspberry Pi το ενεργοποίησα εφόσον το έχει αυτόματα. Μετά σύνδεσα τα 2 συστήματα και αφού είχα πρόσβαση τώρα στα αρχεία τροποποίησα ένα κώδικα python. Στο τέταρτο παραδοτέο έγινε χρήση του ntfy. Αφού το εγκατέστησα έκανα επεξεργασία στο αρχείο .bashrc έτσι ώστε να μου έρχονται ειδοποιήσεις όταν τελειώνει κάτι Για να δείξω ότι λειτουργεί έπαιξα ένα mp3 και στο τέλος μου ήρθε ειδοποίηση. Στο πέμπτο παραδοτέο έκανα χρήση του hyperfine για να ελέγξω το χρόνο εκτέλεσης 2 python προγραμμάτων. Επίσης μαζί με το hyperfine μπορείς να export τις διάφορες πληροφορίες που παίρνεις. Στο έκτο παραδοτέο εφόσον έφτιαξα ένα νέο αποθετήριο με το CV μου μέσα του έβαλα github-pages. Στη συνέχεια έκανα εγκατάσταση του travis-ci. Έφτιαξα το αρχείο .travis.yml έτσι ώστε με οποιαδήποτε αλλαγή να γίνετε αυτόματα build. Τέλος ένωσα το git με το github μου και έκανα push μια αλλαγή και έγινε αυτόματα build. Στο έβδομο παραδοτέο εγκατέστησα το pipenv και virtualenv. Δημιούργησα νέο φάκελο όπου έφτιαξα το νέο Virtual-Enviroment. Ακολούθως το ενεργοποίησα και μέσο της εντολής "which python" και "which pip" δείχνω ότι είναι νέο ανεξάρτητο python enviroment. Μετά έκανα εγκατάσταση τι βιβλιοθήκη math και έφτιαξα και έτρεξα ένα πρόγραμμα που τη χρησιμοποιώ. Στο τελευταίο μου παραδοτέο έκανα χρήση του SpaceVim και NeoVim. Πρώτα έκανα εγκατάσταση του SpaceVim και μετά του Neovim. Το SpaceVim μπαίνει αυτομάτως στο NeoVim μαζί με τα plugins του. Τέλος το άνοιξα και τροποποίησα ένα πρόγραμμα python.

## Αποτελέσματα:
Πιο κάτω είναι τα Asciinema λινκς, screenshots και gifs.
## 1ο παραδοτέο.
### GUAKE
### Asciinema : [guake](https://asciinema.org/a/313444)
### Screenshot
![guake](https://user-images.githubusercontent.com/44147982/77859351-87686e00-7211-11ea-99d9-954180297a15.gif)

### Konsole
### Asciinema : [Konsole](https://asciinema.org/a/313450)
### Screenshot
![konsole](https://user-images.githubusercontent.com/44147982/77859287-25a80400-7211-11ea-9ff8-a29307276670.gif)

### TILDA
### Asciinema : [tilda](https://asciinema.org/a/313451)
### Screenshot
![tilda](https://user-images.githubusercontent.com/44147982/77859310-4b350d80-7211-11ea-9798-0464bab09b89.gif)


### TERMINOLOGY
### Asciinema : [terminology](https://asciinema.org/a/313454)
### Screenshot.
![teminology2](https://user-images.githubusercontent.com/44147982/77859372-a36c0f80-7211-11ea-8da6-9fbd61383782.gif)

### YAKUAKE
### Asciinema : [yakuake](https://asciinema.org/a/314663)
### Εικόνα του τέρμιναλ "yakuake".
![yakuake](https://user-images.githubusercontent.com/44147982/77859447-0eb5e180-7212-11ea-8fed-f4c19b567e80.gif)

### FISH
### Asciinema : [fish](https://asciinema.org/a/313460)
### Screenshot.
![fish](https://user-images.githubusercontent.com/44147982/77859385-b67edf80-7211-11ea-91d6-1553c48ed94d.gif)

### ZSH
### Asciinema : [zsh](https://asciinema.org/a/313467)
### Screenshot.
![zsh](https://user-images.githubusercontent.com/44147982/77859313-4f612b00-7211-11ea-89a9-e4f93f064c55.gif)


## 2ο παραδοτέο.
### Asciinema : [Nginx-Alpine](https://asciinema.org/a/313808)
### Ιστοσελίδα:
![localhost](https://user-images.githubusercontent.com/44147982/77859623-1a55d800-7213-11ea-9830-6937af4649b9.png)



## 3ο παραδοτέο.
### Asciinema : [SSH](https://asciinema.org/a/313829)
### Screenshots
![shh1](https://user-images.githubusercontent.com/44147982/77859749-cc8d9f80-7213-11ea-8c30-bbbff5cf8e56.png)
![ssh2](https://user-images.githubusercontent.com/44147982/77859751-ceeff980-7213-11ea-9b32-0c00db6f7a15.png)
![ssh3](https://user-images.githubusercontent.com/44147982/77859753-d0212680-7213-11ea-9d92-606b6e3a6841.png)


## 4ο παραδοτέο.
### Asciinema : [ntfy](https://asciinema.org/a/313515)
![notification4](https://user-images.githubusercontent.com/44147982/77860015-66a21780-7215-11ea-959a-4c3a9d6831a0.gif)


## 5ο παραδοτέο.
### Asciinema : [hyperfine](https://asciinema.org/a/313484)
### json results
![json results](https://user-images.githubusercontent.com/44147982/77860133-1c6d6600-7216-11ea-961f-fec20de52155.png)


## 6ο παραδοτέο
### Asciinema : [Travis Ci](https://asciinema.org/a/328391)
### Screenshot:
![autobuild Travis](https://user-images.githubusercontent.com/44147982/81502779-a8c87980-92e8-11ea-98a6-550b98cb26e8.png)


## 7ο παραδοτέο
### Asciinema : [Python Virtual Enviroment](https://asciinema.org/a/328394)


## 8ο παραδοτέο
### Asciinema : [Spacevim-Noevim](https://asciinema.org/a/328490)



## Συμπεράσματα:
Αρχίζοντας με τη πρώτη εργασία μπορεί κάποιος να διαπιστώσει ότι με τη αλλαγή του τερμιναλ σου μπορείς να διευκολυνθείς. Συνεχίζοντας στο δεύτερο παραδοτέο βλέποντας τη χρήση του Docker μπορεί κάποιος να ελέγχει έργα μέσα σε Docker και να κάνει δοκιμές μέσα στο ίδιο σύστημα με κάποιον άλλο που δουλεύει στο ίδιο έργο Στο τρίτο παραδοτέο φαίνεται η χρησιμότητα του OpenSSH και πως μπορείς με τη χρήση του να ενώσεις συστήματα και να φτιάξεις δικό σου cloud. Ακολούθως με το ntfy μπορείς να ελέγχεις το πως και πότε να σου έρχονται ιδιοποιήσεις. Με το hyperfine μπορείς να ελέγχεις και να συγκρίνεις τη αποδοτικότητα προγραμμάτων με ευκολία. Μέσο github-pages και travis-ci μπορείς να φτιάξεις σελίδα εύκολα η οποία γίνεται αυτομάτως build και deploy. Με το virtualenv έχεις δικό σου virtual enviroment με το οποίο μπορείς να φτιάξεις προγράμματα και να τα τρέξεις. Τέλος μέσο του SpaceVim το οποίο σου λέει όταν υπάρχει λάθος στο κώδικα μέσο των plugin τους και είναι ένα πολύ χρήσιμο εργαλείο για τη επεξεργασία κωδικά.

### Συμμετοχικό Εκπαιδευτικό Υλικό.

### mibook : [mibook](https://andreaspappoutas.netlify.com)

### Αποθετήριο mibook: [link](https://github.com/andreaspappoutas/gr)
### A.

Η πρώτη είκονα που ανέβασα είναι του iPad.

### [iPad](https://andreaspappoutas.netlify.com/gallery/ipad/)

H δεύτερη εικόνα είναι του Arduino Nano.

### [Arduino Nano](https://andreaspappoutas.netlify.com/gallery/arduino-nano/)


### B.

Στο Β έβαλα ενα διαδραστικό παράδειγμα του MKR1000 dashboard του arduino από το codepen. Είναι ένα παράδειγμα όπου ο χρήστης μπόρει να αλλάξει τις τιμές μέσα στο κώδικα του codepen και να προσέξει πως λειτουργά ενα dashboard του arduino.

### [Arduino Example](https://andreaspappoutas.netlify.app/remix/arduino-example/)
### [Αποθετήριο](https://github.com/andreaspappoutas/gr/blob/master/_remix/arduino-example.md)

### Γ.

Μελέτη περίπτωσης Arduino

### [Arduino Case Study](https://andreaspappoutas.netlify.app/case-study/arduinonew/)
### [Αποθετήριο](https://github.com/andreaspappoutas/gr/blob/master/_case-study/arduinoNew.md)

