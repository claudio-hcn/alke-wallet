# 💳 Alke Wallet – Aplicación Web de Billetera Digital

**Alke Wallet** es una aplicación web que simula el funcionamiento básico de una **billetera digital**, permitiendo a los usuarios registrarse, iniciar sesión, depositar dinero, enviar dinero a contactos y revisar su historial de transacciones.

El proyecto está desarrollado **sin backend**, utilizando **JavaScript puro (ES6)**, **Bootstrap 4**, **jQuery** y **LocalStorage** como mecanismo de persistencia de datos.

👉 **Aplicación en producción (GitHub Pages):**  
🔗 https://claudio-hcn.github.io/alke-wallet/

---

## 🎯 Objetivo del Proyecto

El objetivo principal de este proyecto es:

- Comprender cómo manejar **usuarios, sesiones y datos persistentes** sin backend
- Implementar **lógica financiera básica**
- Simular flujos reales de una aplicación tipo wallet
- Aplicar buenas prácticas de **estructura, validación y experiencia de usuario**
- Trabajar con **LocalStorage** como fuente de datos
- Diseñar una interfaz clara y responsive con Bootstrap

---

## 🔐 Credenciales de Prueba

La aplicación incluye un usuario administrador precargado:

```text
Email: admin@email.com
Password: admin123
Saldo inicial: $100.000

```
También es posible registrar nuevos usuarios desde la pantalla principal.

---

## 🧩 Funcionalidades Detalladas

### 🔑 Autenticación y Sesión
- Registro de nuevos usuarios mediante formulario modal
- Inicio de sesión con validación de credenciales
- Persistencia de sesión usando `localStorage`
- Control de acceso a páginas internas
- Cierre de sesión (logout)
- Usuario administrador precargado

---

### 👤 Gestión de Usuarios
- Usuarios independientes con:
  - Email único
  - Contraseña
  - Saldo propio
  - Contactos propios
  - Historial propio
- Transferencias internas actualizan ambos saldos

---

### 💰 Depósitos
- Página dedicada a depósitos
- Validación del monto ingresado
- Actualización inmediata del saldo
- Registro automático en el historial

---

### 📇 Gestión de Contactos
- Contactos asociados por usuario
- Agregar contactos mediante modal
- Eliminación con confirmación
- Botón eliminar visible solo con selección
- Limpieza automática al hacer click fuera

---

### 💸 Envío de Dinero
- Envío a contactos seleccionados
- Validaciones:
  - Monto válido
  - Saldo suficiente
  - Contacto seleccionado
- Transferencias internas:
  - Descuento al emisor
  - Aumento al receptor
  - Registro en ambos historiales

---

### 📜 Historial de Transacciones
- Historial independiente por usuario
- Tipos:
  - Depósito
  - Envío
  - Recepción
- Información mostrada:
  - Tipo
  - Monto
  - Fecha
  - Contacto
- Paginación (5 movimientos por página)
- Mensaje si no hay movimientos

---

## 🎨 Interfaz de Usuario

- Bootstrap 4
- Diseño responsive
- Modales para:
  - Registro
  - Agregar contactos
- Navegación clara
- Botones grandes y visibles

---

## 🛠️ Tecnologías Utilizadas

- HTML5
- CSS3
- Bootstrap 4
- JavaScript ES6
- jQuery
- LocalStorage

---

## 📂 Estructura del Proyecto

```text
/
├── index.html
├── menu.html
├── depositar.html
├── enviar-dinero.html
├── historial.html
├── README.md
```
## 💾 Persistencia de Datos

La aplicación utiliza **LocalStorage** como mecanismo de almacenamiento, permitiendo que los datos persistan incluso al recargar la página.

Se almacenan los siguientes elementos:

- `users`: usuarios registrados
- `currentUserId`: sesión activa
- `contactos_{idUsuario}`: contactos por usuario
- Saldos y movimientos por usuario

📌 Todos los datos se guardan **solo en el navegador** del usuario.

---

## 🔄 Reiniciar la Aplicación

Si deseas comenzar desde cero y borrar todos los datos almacenados, ejecuta el siguiente comando en la consola del navegador:

```js
localStorage.clear();
location.reload();
```

### Esto eliminará:

Usuarios

Sesiones

Contactos

Historial de movimientos