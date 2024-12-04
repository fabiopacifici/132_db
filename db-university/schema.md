> Esercizio di oggi:

nome repo: **db-university**

Modellizzare la struttura di un database per memorizzare tutti i dati riguardanti una università:

- sono presenti diversi `Dipartimenti` (es.: Lettere e Filosofia, Matematica, Ingegneria ecc.);
- ogni `Dipartimento` offre più `Corsi di Laurea` (es.: Civiltà e Letterature Classiche, Informatica, Ingegneria Elettronica ecc..)
- ogni `Corso di Laurea` prevede diversi `Corsi` (es.: Letteratura Latina, Sistemi Operativi 1, Analisi Matematica 2 ecc.);
- ogni `Corso` può essere tenuto da diversi `Insegnanti`;
- ogni `Corso` prevede più appelli d'`Esame`;
- ogni `Studente` è iscritto ad un solo `Corso di Laurea`;
- ogni `Studente` può iscriversi a più appelli di `Esame`;
- per ogni appello d'`Esame` a cui lo `Studente` ha partecipato, è necessario memorizzare il voto ottenuto, anche se non sufficiente.
Pensiamo a quali entità (tabelle) creare per il nostro database e cerchiamo poi di stabilirne le relazioni. Infine, andiamo a definire le colonne e i tipi di dato di ogni tabella.

Utilizzare <https://www.drawio.com/> per la creazione dello schema.
Esportare quindi il diagramma in jpg e caricarlo nella repo.
>

## Table: departments

- id
- name
- head_of_department
- website
- phone
- email_address

## Table: degrees (one to many -> departments)

- id
- department_id (FK)
- name
- description
- period

## Table: courses (one to many -> degree)

- id
- degree_id (FK)
- name
- description

## Pivot: course_teacher

- course_id (FK)
- teacher_id (FK)

## Table: teachers

- id
- name
- lastname
- office_number
- mobile_number

## Table: exams

- id
- course_id (FK)
- date
- hour

## Pivot: exam_student

- student_id
- exam_id
- vote

## Table: students (one to many -> degrees)

- id
- degree_id
- name
- lastname
- email
- phone
- enrolment_date
- registration_number

PDTA - Department of Planning, Design, and Technology of Architecture
