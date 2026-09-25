FINANZAS FAMILIA — INSTALACIÓN SIN NODE.JS

1) En Firebase Console crea un proyecto.
2) Agrega una aplicación Web.
3) Activa Authentication > Sign-in method > Email/Password.
4) Crea Firestore Database.
5) En Firebase Console > Firestore > Rules, pega el contenido de firebase-rules.txt.
6) Abre index.html y busca "const firebaseConfig".
7) Sustituye los valores PEGA_... por los datos que entrega Firebase en Project settings > Your apps > Web.
8) Sube estos archivos a GitHub desde el navegador.
9) Publica el repositorio con Firebase Hosting según el método disponible en tu cuenta/proyecto.
10) Abre la URL HTTPS en Chrome del celular y usa "Instalar aplicación" / "Agregar a pantalla de inicio".

IMPORTANTE:
- La configuración web de Firebase no contiene una contraseña secreta. La seguridad real está en Authentication + Firestore Rules.
- Para que Alfredo y Lisbeth compartan exactamente los mismos datos, la versión siguiente debe usar una familia compartida (familyId) y reglas por pertenencia, no solamente por UID.
- Esta versión inicial guarda cada usuario en su propio espacio. NO usarla todavía como versión familiar compartida hasta implementar familyId.
