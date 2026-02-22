# Odoo Financial Module 🏦 | ERP Customization & Business Logic

Este repositorio contiene un módulo personalizado para **Odoo 16** diseñado para la gestión de entidades bancarias, movimientos y clientes. El proyecto se centra en la implementación de reglas de negocio complejas y la extensión de modelos base del ERP.

---

## 🛠️ Funcionalidades Técnicas

### 1. Extensión de Modelos Core
* **Inheritance:** Extensión del modelo base `res.user` (Customer) mediante Python para integrar validaciones financieras y campos relacionales sin usar el modo desarrollador de la UI.
* **Integridad Referencial:** Implementación de controles preventivos en el borrado de cuentas para evitar errores `HTTP 500`, garantizando que solo se eliminen cuentas sin historial de movimientos.

### 2. Lógica de Negocio Avanzada
* **Sistema "Undo" de Movimientos:** Lógica personalizada para permitir solo el borrado del último movimiento, con recalculación automática y atómica del balance de la cuenta.
* **Validaciones Condicionales:** Restricciones de edición en campos sensibles (`description`, `creditLine`) basadas en el tipo de cuenta (CREDIT/DEBIT).
* **Cálculos Automáticos:** Implementación de @api.depends para la actualización en tiempo real de saldos y estados financieros.

---

## 🏗️ Stack Tecnológico
- **Core:** Python 3
- **Framework:** Odoo 16 (ORM & Web Framework)
- **Data:** XML (Vistas y menús), CSV (Carga de datos maestros)

---

## 👤 Autor
**Aitor Jury Rodríguez** - *Fullstack Developer & Intern @ BBVA Technology*
- [LinkedIn](https://www.linkedin.com/in/aitor-jury-rodr%C3%ADguez-6330742b1/)
- [Email](mailto:aitor.jr04@gmail.com)
