---
title: Acceso a bases de datos en Yii
author: Ricardo Pérez López
!DATE
---

# DAO

## `yii\db\Connection`

## `yii\db\Connection::createCommand()`

## Consultas SQL

### `queryAll()`

### `queryOne()`

### `queryColumn()`

### `queryScalar()`

## Sentencias no `SELECT`

### `execute()`

### `insert()`

### `update()`

### `delete()`

# Query Builder

## `yii\db\Query`

## Creación de consultas

### `select()`

### `from()`

### Condiciones y filtrado de filas

#### `where()`

#### Formatos de condiciones

##### De cadena

##### De array

##### De operadores

#### `andWhere()`

#### `orWhere()`

#### `filterWhere()`

#### `andFilterWhere()`

#### `orFilterWhere()`

### `orderBy()`

### `groupBy()`

### Condiciones y filtrado de grupos

#### `having()`

#### `filterHaving()`

#### `andFilterHaving()`

#### `orFilterHaving()`

### `limit()`

### `offset()`

### Combinaciones

#### `join()`

#### `innerJoin()`

#### `leftJoin()`

#### `rightJoin()`

### `union()`

## Recogida de resultados

### `all()`

### `one()`

### `column()`

### `scalar()`

### `exists()`

### `count()`

### Funciones de grupo

#### `sum()`

#### `average()`

#### `max()`

#### `min()`

### `indexBy()`

## Consultas por lotes

### `batch()`

### `each()`

# Active Record

## `findOne()`

## `findAll()`

## `save()`

## ActiveQuery

### `find()`

## Atributos sucios

## Relaciones

### Encadenamiento de relaciones

## `joinWith()`

## Atributos virtuales

### Siete técnicas

#### Calcular a mano cuando/donde haga falta

#### Usar vistas SQL

#### Sobreescribir el método `find()` del modelo para que se use siempre en lugar del heredado de `ActiveRecord`

#### Sobreescribir el método `afterFind()` para rellenar el atributo a mano cada vez que se hace un `find()`

#### Capturar el evento `EVENT_AFTER_FIND` del modelo

#### Usar una propiedad con *getter* y *setter*

#### Crear un método `findEspecial()` que se usará en lugar de `find()` cuando haga falta

#### La mejor opción, en la mayoría de los casos: combinar las dos anteriores

##### Ejemplo

# Metadatos

## Objetivos de la unidad

## Resultados de aprendizaje y criterios de evaluación asociados

### RA2

### RA3

### RA4

#### CE4.g

### RA5

#### CE5.f

#### CE5.g

#### CE5.h

### RA6

#### CE6.a

#### CE6.b

#### CE6.c

#### CE6.d

#### CE6.e

#### CE6.f

#### CE6.g

#### CE6.h

### RA9

#### CE9.e

#### CE9.f

#### CE9.g

