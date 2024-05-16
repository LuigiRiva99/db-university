# QUERY con GROUP BY
1. Contare quanti iscritti ci sono stati ogni anno
    - SELECT COUNT(*) AS `numero_iscrizioni`, YEAR(`enrolment_date`) AS `anno_iscrizione` FROM `students` GROUP BY YEAR(`enrolment_date`);    
2. Contare gli insegnanti che hanno l'ufficio nello stesso edificio

3. Calcolare la media dei voti di ogni appello d'esame

4. Contare quanti corsi di laurea ci sono per ogni dipartimento


# QUERY con JOIN
5. Selezionare tutti gli studenti iscritti al Corso di Laurea in Economia

6. Selezionare tutti i Corsi di Laurea Magistrale del Dipartimento di
Neuroscienze

7. Selezionare tutti i corsi in cui insegna Fulvio Amato (id=44)

8. Selezionare tutti gli studenti con i dati relativi al corso di laurea a cui
sono iscritti e il relativo dipartimento, in ordine alfabetico per cognome e
nome

9. Selezionare tutti i corsi di laurea con i relativi corsi e insegnanti

10. Selezionare tutti i docenti che insegnano nel Dipartimento di
Matematica (54)

