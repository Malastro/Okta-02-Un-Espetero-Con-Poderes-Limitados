# Okta 02 — Un espetero con poderes limitados

## 1. Descripción del proyecto

Este laboratorio está inspirado en el episodio 7x04 de *La que se avecina*: **«Un espetero-hostelero, una agonía rural y unas gotitas de burundanga»**.

Fermín Trujillo, el espetero más peculiar de Mirador de Montepinar, se pone al frente del Max & Henry dispuesto a demostrar que también puede triunfar en el mundo de la hostelería. Para darle un impulso al negocio, decide organizar una fiesta de Halloween que termina convirtiéndose en un auténtico descontrol.

Trasladamos esta situación al entorno digital de **Mirador de Montepinar S. L.**, donde Fermín necesita gestionar las cuentas de los empleados y colaboradores de su establecimiento. Hasta ahora, cualquier modificación de usuarios debía realizarla un administrador general de la organización, incluso cuando se trataba de operaciones sencillas relacionadas exclusivamente con el bar.

Para agilizar estas tareas, surge una propuesta aparentemente razonable: conceder a Fermín permisos administrativos en Okta.

Sin embargo, entregar privilegios excesivos a alguien que acaba de hacerse cargo del Max & Henry podría provocar un problema de seguridad. Fermín no necesita administrar las cuentas de Mariscos Recio, modificar las identidades de los miembros de la Junta de Gobierno ni intervenir en las políticas de autenticación de toda la comunidad.

Ante esta situación, Enrique Pastor propone establecer un modelo de **administración delegada basado en el principio de mínimo privilegio**, de manera que Fermín pueda realizar únicamente las operaciones necesarias sobre las identidades vinculadas a su negocio.

El objetivo del laboratorio es implementar y validar este modelo mediante **Custom Admin Roles y Resource Sets de Okta**, definiendo tanto las operaciones administrativas permitidas como los recursos sobre los que pueden ejecutarse.

A través de distintas pruebas, se comprobará si Fermín puede consultar y modificar las identidades de su ámbito de responsabilidad, mientras se restringen las operaciones sobre usuarios ajenos al Max & Henry y las funciones administrativas que no necesita.

También se investigarán los riesgos asociados a la edición de atributos de identidad. En particular, se estudiará si una delegación demasiado amplia podría afectar indirectamente a las pertenencias automáticas configuradas en el laboratorio anterior, donde el atributo `cargoVecinal` determina quién pertenece a `Junta de Gobierno`.

Las pruebas incluirán operaciones autorizadas y denegadas, la comprobación de los permisos efectivos desde la cuenta de Fermín y la revisión de los eventos disponibles en **System Log**.

Este laboratorio permitirá profundizar en conceptos de *Identity and Access Management (IAM)* como **Role-Based Access Control (RBAC)**, administración delegada, separación de responsabilidades y mínimo privilegio.

**Escenario ficticio:** Mirador de Montepinar S. L., donde Fermín Trujillo acaba de descubrir que dirigir un bar también implica gestionar usuarios y permisos. Porque una cosa es darle las llaves del Max & Henry y otra muy distinta es permitirle administrar todo Montepinar.
