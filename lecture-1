DROP TABLE classmates, pets CASCADE;

CREATE TABLE classmates (
  id INT PRIMARY KEY,
  first_name VARCHAR(255) NOT NULL,
  last_name VARCHAR(255),
  email VARCHAR(255)
);

-- INSERT

INSERT INTO classmates VALUES (1, 'Arvid', 'Berndtsson', 'arvid@berndtsson.me');

INSERT INTO classmates (id, email, first_name, last_name) VALUES (2, 'ellie@ell.gg', 'Ellie', 'Fagerberg');

INSERT INTO classmates (id, email, first_name) VALUES
    (3, 'hannah@lindback.se', 'Hannah'),
    (4, NULL, 'Andy'),
    (5, 'simone@jonsson.se', 'Simone');

-- SELECT

SELECT * FROM classmates;

SELECT first_name, last_name FROM classmates;

SELECT first_name, last_name FROM classmates WHERE email = 'ellie@ell.gg';

SELECT first_name, last_name FROM classmates WHERE LOWER(email) LIKE 'arvid%';

-- UPDATE

UPDATE classmates SET email = 'ellie@elliestudios.com' WHERE id = 2;

UPDATE classmates SET first_name = 'Hanna', email = 'hanna@lindback.se' WHERE email = 'hannah@lindback.se';

-- DELETE

DELETE FROM classmates WHERE id = 5;

DELETE FROM classmates WHERE email IS NULL;

-- CREATE

DROP TABLE IF EXISTS classmates CASCADE;

CREATE TABLE classmates (
  id INT PRIMARY KEY,
  first_name VARCHAR(255) NOT NULL,
  last_name VARCHAR(255),
  email VARCHAR(255)
);

-- ALTER

ALTER TABLE classmates ADD COLUMN age INT;

ALTER TABLE classmates ALTER COLUMN email SET NOT NULL;

ALTER TABLE classmates ALTER COLUMN email DROP NOT NULL;

-- Foreign keys

CREATE TABLE pets (
  id INT PRIMARY KEY,
  name VARCHAR(255) NOT NULL,
  owner_id INT NOT NULL,
  FOREIGN KEY (owner_id) REFERENCES classmates(id)
);
