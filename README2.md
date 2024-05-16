# QUERY con GROUP BY
1. Contare quanti iscritti ci sono stati ogni anno
    - SELECT COUNT(*) AS `numero_iscrizioni`, YEAR(`enrolment_date`) AS `anno_iscrizione` FROM `students` GROUP BY YEAR(`enrolment_date`);    
2. Contare gli insegnanti che hanno l'ufficio nello stesso edificio
    - SELECT `office_address`, COUNT(*) AS `insegnanti_nell'edificio` FROM `teachers` GROUP BY `office_address`; 
3. Calcolare la media dei voti di ogni appello d'esame
    - SELECT `exams`.`date`, AVG(`exam_student`.`vote`) AS `media_voto` FROM `exam_student` INNER JOIN `exams` ON `exam_student`.`exam_id` = `exams`.`id` GROUP BY `exams`.`date`; 
4. Contare quanti corsi di laurea ci sono per ogni dipartimento
    - SELECT `departments`.`name`, COUNT(*) AS `numero_corsi_di_laurea` FROM `departments` INNER JOIN `degrees` ON `departments`.`id` = `degrees`.`department_id` GROUP BY `departments`.`name`; 

# QUERY con JOIN
5. Selezionare tutti gli studenti iscritti al Corso di Laurea in Economia
    - SELECT `degrees`.`name`, `students`.* FROM `degrees` INNER JOIN `students` ON `degrees`.`id` = `students`.`degree_id` WHERE `degrees`.`name` = 'Corso di Laurea in Economia'; 
6. Selezionare tutti i Corsi di Laurea Magistrale del Dipartimento di
Neuroscienze
    - SELECT * FROM `departments` INNER JOIN `degrees` ON `departments`.`id` = `degrees`.`department_id` WHERE `departments`.`name` = 'Dipartimento di Neuroscienze' AND `degrees`.`level` = 'magistrale'; 
7. Selezionare tutti i corsi in cui insegna Fulvio Amato (id=44)

8. Selezionare tutti gli studenti con i dati relativi al corso di laurea a cui
sono iscritti e il relativo dipartimento, in ordine alfabetico per cognome e
nome

9. Selezionare tutti i corsi di laurea con i relativi corsi e insegnanti

10. Selezionare tutti i docenti che insegnano nel Dipartimento di
Matematica (54)

