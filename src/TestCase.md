## Test case: User- Înregistrare utilizator nou

| Scop                                         | Cerință                                                | Pas | Descrierea pasului                                                            | Rezultatul așteptat                       | Rezultatul așteptat final | Status |
|----------------------------------------------|--------------------------------------------------------|-----|-------------------------------------------------------------------------------|-------------------------------------------|---------------------------|--------|
| Verificarea funcționalității de înregistrare a unui utilizator nou în sistem. | Utilizatorul trebuie să fie capabil să înregistreze un user nou. | 1   | Accesează pagina de înregistrare a utilizatorilor. | Pagina de înregistrare este deschisă.     |Utilizatorul este înregistrat cu succes în sistem și poate să se autentifice utilizând datele de autentificare completate în timpul înregistrării.| N/A    |
|                                              |                                                        | 2   | Completează toate câmpurile obligatorii cu date valide (nume, prenume, adresă de email, parolă, confirmare parolă).| Câmpurile sunt completate.  |  | N/A    |
|                                              |                                                        | 3   | Apasă pe butonul "Înregistrare" sau "Crează cont". |Userul este înregistrat și pagina este afișată. | | N/A    |

---

## Test case: User- Înregistrare negativa a utilizatorului nou

| Scop                                         | Cerință                                                | Pas | Descrierea pasului                                                            | Rezultatul așteptat                       | Rezultatul așteptat final                                     | Status |
|----------------------------------------------|--------------------------------------------------------|-----|-------------------------------------------------------------------------------|-------------------------------------------|--------------------------------------------------------------|--------|
| Verificarea comportamentului sistemului în cazul în care utilizatorul încearcă să se înregistreze folosind date invalide sau lipsă. | Numele utilizatorului trebuie să fie de lungimea cel puțin 8 caractere, iar parola maxim 12 caractere. | 1   | Accesează pagina de înregistrare a utilizatorilor. | Pagina de înregistrare este deschisă.     | Sistemul afișează mesaje de eroare corespunzătoare pentru câmpurile completate incorect sau lipsă. Utilizatorul nu este înregistrat în sistem și este redirecționat înapoi către pagina de înregistrare pentru a corecta datele introduse. | N/A    |
|                                              |                                                        | 2   | Completează câmpul username obligatoriu cu date invalide sau lasă câmpuri necompletate (ex. "Maadwuh3", "manhqbc3", "MANTHSL3", "MANYYWBD N", "15785155"). | Apare mesajul cu date incorecte.          | Utilizatorul nu este înregistrat în sistem și este redirecționat înapoi către pagina de înregistrare pentru a corecta datele introduse. | N/A    |
|                                              |                                                        | 3   | Completează câmpul parolă obligatoriu cu date invalide sau lasă câmpuri necompletate. | Apare mesajul cu date incorecte.          | | N/A    |
|                                              |                                                        | 4   | Apasă pe butonul "Înregistrare" sau "Crează cont".    | Utilizatorul nu este înregistrat în sistem și este redirecționat înapoi către pagina de înregistrare pentru a corecta datele introduse. |  | N/A    |


---

## Test case: User- Autentificare utilizator

| Scop                                         | Cerințe                                                | Pas | Descrierea pasului                                   | Rezultatul așteptat    | Rezultatul așteptat final | Status |
|----------------------------------------------|--------------------------------------------------------|-----|------------------------------------------------------|------------------------|-|--------|
| Verificarea funcționalității de autentificare a unui utilizator în sistem. | Utilizatorul trebuie să fie capabil să se logheze cu date valide. | 1   | Accesează pagina de autentificare a utilizatorilor. | Pagina de autentificare este deschisă. | Utilizatorul este autentificat cu succes în sistem și are acces la funcționalitățile aferente rolului său (exemplu: gestionarea profilului, vizualizarea informațiilor personale etc.). | N/A    |
|                                              |                                                        | 2   | Completează câmpurile de autentificare (adresă de email și parolă) cu datele valide ale unui utilizator înregistrat în sistem. | User logat cu succes. | | N/A    |
|                                              |                                                        | 3   | Testarea cu lungimea minimă pentru username și parolă | Bifa devine verde, datele sunt cele așteptate de sistem. | | N/A    |
|                                              |                                                        | 4   | Testarea cu username și parolă cu caractere alfanumerice și cifre, aparte fiecare | Bifa verde. | | N/A    |
|                                              |                                                        | 5   | Apasă pe butonul "Autentificare" sau "Log in". | Utilizator autentificat cu succes. | | N/A    |

---
## Test case: Autentificare negativă a utilizatorului

| Scop                                         | Cerințe                                                | Pas | Descrierea pasului                                                            | Rezultatul așteptat                       | Rezultatul așteptat final | Status |
|----------------------------------------------|--------------------------------------------------------|-----|-------------------------------------------------------------------------------|-------------------------------------------|-----------------------|--------|
| Verificarea comportamentului sistemului în cazul în care utilizatorul încearcă să se autentifice folosind date de autentificare invalide. | Numele utilizatorului trebuie să fie cel puțin 8 caractere, iar parola maxim 12 caractere. | 1   | Accesează pagina de autentificare a utilizatorilor. | Pagina de autentificare este deschisă.     | Sistemul afișează un mesaj de eroare corespunzător în cazul datelor de autentificare incorecte. Utilizatorul nu este autentificat în sistem și rămâne pe pagina de autentificare pentru a corecta datele introduse. | N/A    |
|                                              |                                                        | 2   | Completează câmpului username de autentificare cu adresă de email cu date invalide sau inexistente sau lasă câmpuri necompletate pentru un utilizator înregistrat în sistem (ex. "3postaMold@.48", "postaMOLD.48", "52258585@.com") | Mesaj de eroare afișat.          | Utilizatorul nu este autentificat în sistem și rămâne pe pagina de autentificare pentru a corecta datele introduse. | N/A    |
|                                              |                                                        | 3   | Completează câmpul parolă obligatoriu cu date invalide sau lasă câmpuri necompletate. | Apare mesajul cu date incorecte.          | | N/A    |
|                                              |                                                        | 4   | Apasă pe butonul "Autentificare" sau "Log in".    | Mesaj de eroare afișat și întors înapoi la pagina de logare.          || N/A    |


---

## Test Case: Sistem de votare pentru postări

| Scop                                         | Cerințe                                                | Pas | Descrierea pasului                                                            | Rezultatul așteptat                       | Rezultatul așteptat final | Status |
|----------------------------------------------|--------------------------------------------------------|-----|-------------------------------------------------------------------------------|-------------------------------------------|-------------------------|--------|
| Verificarea formării postărilor pe platformă. | Postarea trebuie să poate fi accesată și să se scrie un comentariu. | 1   | Autentifică-te în sistem ca utilizator valid. - Pagina generală a fost deschisă. | Pagina generală este deschisă.     | Postarea a fost creată cu succes de către utilizator și poate fi vizualizată de către alți utilizatori. | N/A    |
|                                              |                                                        | 2   | Accesează secțiunea de creare postare din tema selectată. - Fereastra de comentariu este disponibilă. | Fereastra de comentariu este disponibilă.          | | N/A    |
|                                              |                                                        | 3   | Completează câmpurile obligatorii pentru titlu. - Câmpul cu titlu este accesibil. | Câmpul cu titlu este accesibil.          |  | N/A    |
|                                              |                                                        | 4   | Completează câmpurile obligatorii pentru conținut. - Câmpul conținut este accesibil. | Câmpul conținut este accesibil.          || N/A    |
|                                              |                                                        | 5   | Completează câmpurile pentru alte detalii precum importarea din fișier, stickere. - Câmpul detalii este accesibil, mapa cu fișiere de pe PC este accesată cu succes. | Câmpul detalii este accesibil, fișierele au fost accesate cu succes.          | | N/A    |
|                                              |                                                        | 6   | Apasă pe butonul "Postează" sau "Crează postare".    | Postarea a fost creată și poate fi vizualizată.          | | N/A    |

---

## Test Case: Votarea cu succes a postării create de useri

| Scop                                         | Cerințe                                                | Pas | Descrierea pasului                                                   | Rezultatul așteptat                    | Rezultatul așteptat final | Status |
|----------------------------------------------|--------------------------------------------------------|-----|----------------------------------------------------------------------|----------------------------------------|------------------------|--------|
| Verificarea comportamentului sistemului în cazul în care utilizatorul încearcă să se autentifice folosind date de autentificare invalide. | Postarea trebuie să existe și să poată fi apreciată. | 1   | Autentifică-te în sistem ca utilizator valid. | User există, intrarea pe pagina principală.   | Postarea poate fi apreciată cu vot pozitiv sau cu vot negativ, sistemul trebuie să calculeze corect votul pozitiv sau negativ și să îl afișeze pentru a putea fi vizualizat de alți utilizatori. | N/A    |
|                                              |                                                        | 2   | Accesează o postare existentă din tema selectată. - Postarea poate fi accesată. | Postarea poate fi accesată.          |  | N/A    |
|                                              |                                                        | 3   | Acordă un vot pozitiv (upvote) postării. | Votul pozitiv a fost plasat +1 la suma voturilor postării. | | N/A    |
|                                              |                                                        | 4   | Acordă un vot negativ (downvote) postării.| Votul negativ a fost plasat -1 la suma voturilor postării. | | N/A    |
|                                              |                                                        | 5   | Verifică că sistemul permite acordarea unui singur vot pentru fiecare postare și actualizează numărul de voturi. | Un user plasează doar un vot, nu două. |  | N/A    |

---

## Test Case: Vizibilitate și clasificare

| Scop                                         | Cerințe                                                | Pas | Descrierea pasului                                                         | Rezultatul așteptat                       | Rezultatul așteptat final | Status |
|----------------------------------------------|--------------------------------------------------------|-----|----------------------------------------------------------------------------|-------------------------------------------|--------------|--------|
| Verificarea vizibilității și clasificării postărilor pe platformă. | Postarea trebuie să fie vizibilă și să fie clasificată cu numărul de voturi. | 1   | Accesează secțiunea de vizualizare postări din tema selectată. | Secțiunea a fost deschisă cu succes.    | Postările sunt vizibile de utilizatori și sunt sortate în secțiunea de sortare conform sumei totale de voturi pe care o deține postarea. | N/A    |
|                                              |                                                        | 2   | Verifică că postările sunt afișate în ordinea corectă în funcție de numărul total de voturi, cu cele mai votate postări în partea superioară a listei. | Postările au fost afișate cu succes conform numărului total de voturi.         |  | N/A    |


---

## Test Case: Editare și ștergere postare

| Scop                                         | Cerințe                                                | Pas | Descrierea pasului                                                          | Rezultatul așteptat                  | Rezultatul așteptat final | Status |
|----------------------------------------------|--------------------------------------------------------|-----|-----------------------------------------------------------------------------|--------------------------------------|-------------|--------|
| Verificarea funcționalității de editare și ștergere a postărilor de către utilizatori și administratori. | Postarea poate fi editată și ștearsă. | 1   | Autentifică-te în sistem ca utilizator valid sau ca administrator.  | User existent, admin existent, logare cu succes. | Postarea este modificată de către proprietarul postării, ștearsă de către proprietarul postării și de către admin dacă postarea a încălcat regulile generale de scriere a postărilor. | N/A    |
|                                              |                                                        | 2   | Accesează postarea proprie sau postările din temele pentru care ai drepturi de editare și ștergere. | Postarea poate fi accesată din partea proprietarului postării și a adminului responsabil de temă.     |  | N/A    |
|                                              |                                                        | 3   | Incercare Editează conținutul postării și verifică că modificările sunt salvate corect. |  insucces     |  | N/A    |
|                                              |                                                        | 4   | Incercare Șterge o postare și verifică că aceasta nu mai apare în lista de postări. |  insucces.     |  | N/A    |
|                                              |                                                        | 5   | Autentifică-te în sistem ca utilizator valid sau ca administrator. |     | | N/A    |
|                                              |                                                        | 6   | Accesează postarea proprie sau postările din temele pentru care ai drepturi de editare și ștergere. |Postarea poate fi accesată din partea proprietarului postării și a adminului responsabil de temă.    |  | N/A    |
|                                              |                                                        | 7   | Editează conținutul postării și verifică că modificările sunt salvate corect. | Conținutul poate fi modificat și se salvează cu succes din partea user, admin nu are drept de modificare a postărilor userilor.     |  | N/A    |
|                                              |                                                        | 8   | Șterge o postare și verifică că aceasta nu mai apare în lista de postări. | Postarea este ștearsă cu succes și nu mai apare în lista postărilor.     | | N/A    |
|                                              |                                                        | 9   | Autentifică-te în sistem ca utilizator valid sau ca administrator. | Utilizatorul/administratorul este autentificat cu succes.     |  | N/A    |
|                                              |                                                        | 10  | Accesează postarea proprie sau postările din temele pentru care ai drepturi de editare și ștergere. | Postarea poate fi accesată din partea proprietarului postării și a adminului responsabil de temă.    |  | N/A    |
|                                              |                                                        | 11  | Editează conținutul postării și verifică că modificările sunt salvate corect. | Conținutul poate fi modificat și se salvează cu succes din partea user, admin nu are drept de modificare a postărilor userilor. |  | N/A    |
|                                              |                                                        | 12  | Șterge o postare și verifică că aceasta nu mai apare în lista de postări. | Postarea poate fi ștearsă din partea proprietarului postării și a adminului temei și postarea nu mai apare în lista postărilor.    | | N/A    |


---

## Test Case: Gestionarea voturilor

| Scop                                                              | Cerințe                                                           | Pas | Descrierea pasului                                                               | Rezultatul așteptat                                         | Rezultatul așteptat final | Status |
|-------------------------------------------------------------------|-------------------------------------------------------------------|-----|----------------------------------------------------------------------------------|--------------------------------------------------------------|---------------------------|--------|
| Verificarea corectitudinii sistemului de gestionare a voturilor pentru postări. | Numărul total de voturi este numărat corect de sistem. | 1   | Autentifică-te în sistem ca utilizator valid sau ca administrator. | User, admin existent, logare de succes.     | Sistemul de votare pentru postări funcționează corect, permițând utilizatorilor să vizualizeze și să voteze postările după criteriul de numărul de voturi. La accesarea upvote sau downvote, numărul total de voturi se modifică corect. | N/A    |
|                                                                   |                                                                   | 2   | Accesează secțiunea de gestionare a voturilor pentru postări. |  Accesare cu succes la secțiunea cu postări.   |  | N/A    |
|                                                                   |                                                                   | 3   | Verifică că sistemul permite vizualizarea și administrarea voturilor acordate postărilor (upvotes și downvotes). | Se poate de văzut postarea și de adăugat vot pozitiv sau vot negativ.        | | N/A    |
|                                                                   |                                                                   | 4   | Verifică că numărul total de voturi pentru fiecare postare este afișat corect și poate fi actualizat. | Tastarea butonului cu upvote și +1 vot la suma totală; Tastarea butonului cu downvote și -1 vot la suma totală de voturi.  |  | N/A    |
