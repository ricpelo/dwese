---
title: Persistencia de datos con PHP
author: Ricardo Pérez López
!DATE
---

# PDO (PHP Data Objects)

## Clase `PDO`

### `__construct(string $dsn [, string $username [, string $password [, array $options ]]])`

### `PDOStatement query(string $statement)`

### `int exec(string $statement)`

### `PDOStatement prepare(string $statement [, array $driver_options = array() ])`

## Clase `PDOStatement`

### `mixed fetch([ int $fetch_style ])`

### `mixed fetchAll([ int $fetch_style ])`

### `mixed fetchColumn([ int $column_number = 0 ])`

### `bool execute ([ array $input_parameters ])`

### `int rowCount(void)`

## Correspondencias de tipos entre SQL y PHP

## Transacciones

### `$pdo->beginTransaction();`

### `$pdo->commit();`

### `$pdo->rollBack();`

# Cookies

## `setcookie()`

## Ejemplos de uso

# Sesiones

## Iniciar una sesión

### `session_start()`

## Usar una sesión

### `$_SESSION`

### Ejemplos de uso

## Terminar una sesión

### `session_destroy()`

### `session_name()`

### `session_id()`

### `session_get_cookie_params()`

# Seguridad y persistencia

## Contraseñas

### https://www.md5online.org/

### https://www.sha1online.org/

### `password_hash()`

### `password_verify()`

## Inyección de código SQL

## Cross-Site Request Forgery (CSRF)

# Meta

## Objetivos de la unidad

## Resultados de aprendizaje y criterios de evaluación asociados

### RA2

### RA3

### RA4

#### CE4.a

#### CE4.b

#### CE4.c

#### CE4.d

#### CE4.e

### RA5

#### CE5.f

#### CE5.g

### RA6

#### CE6.a

#### CE6.b

#### CE6.c

#### CE6.d

#### CE6.e

#### CE6.f

#### CE6.g

# Metadatos

## Objetivos de la unidad

## Resultados de aprendizaje y criterios de evaluación asociados

### RA2

### RA3

### RA4

#### CE4.a

#### CE4.b

#### CE4.c

#### CE4.g

### RA5

#### CE5.f

#### CE5.g

#### CE5.h

### RA6

#### CE6.a

#### CE6.b

#### CE6.c

#### CE6.e

#### CE6.g

