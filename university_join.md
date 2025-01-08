# Esercizio

1. Selezionare tutti gli studenti iscritti al Corso di Laurea in Economia

SELECT
`students`.`id` `students_id`,
`students`.`name` `students_name`,
`students`.`surname` `students_surname`,
`degrees`.`name` `degrees_name`
FROM students
INNER JOIN degrees
ON `degrees`.`name` = 'Corso di Laurea in Economia';

2. Selezionare tutti i Corsi di Laurea Magistrale del Dipartimento di
   Neuroscienze

SELECT
`degrees`.`id` `degrees_id`,
`degrees`.`name` `degrees_name`,
`degrees`.`level` `degrees_level`,
`departments`.`id` `departments_id`,
`departments`.`name` `departments_name`
FROM degrees
INNER JOIN departments
ON `departments`.`name` = 'Dipartimento di Neuroscienze';

3. Selezionare tutti i corsi in cui insegna Fulvio Amato (id=44)

SELECT
`courses`.`name` `courses_name`,
`teachers`.`name` `teachers_name`,
`teachers`.`surname` `teachers_surname`
FROM courses
INNER JOIN teachers
ON `teachers`.`id` = 44;

4. Selezionare tutti gli studenti con i dati relativi al corso di laurea a cui
   sono iscritti e il relativo dipartimento, in ordine alfabetico per cognome e
   nome

   SELECT \*
   FROM students
   INNER JOIN degrees
   ON `students`.`degree_id` =`degrees`.`id`
   INNER JOIN departments
   ON `departments`.`id`;

5. Selezionare tutti i corsi di laurea con i relativi corsi e insegnanti

SELECT \*
FROM degrees
INNER JOIN courses
ON `courses`.`id`
INNER JOIN teachers
ON `teachers`.`id`;

6. Selezionare tutti i docenti che insegnano nel Dipartimento di
   Matematica (54)

7. BONUS: Selezionare per ogni studente il numero di tentativi sostenuti
   per ogni esame, stampando anche il voto massimo. Successivamente,
   filtrare i tentativi con voto minimo 18.
