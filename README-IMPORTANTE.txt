FINANZAS FAMILIA — VERSIÓN COMPARTIDA (Alfredo y Lisbeth ven los mismos datos)

QUÉ CAMBIÓ RESPECTO A LA VERSIÓN ANTERIOR:
- Antes cada cuenta veía solo sus propios movimientos. Ahora TODAS las
  cuentas autenticadas de tu proyecto ven y registran los mismos datos
  (transacciones, meta de ahorro).
- La app YA NO permite crear cuentas nuevas desde el formulario (solo
  "Iniciar sesión"). Esto es a propósito: así nadie ajeno puede
  registrarse aunque descubra la URL. Tú creas las cuentas manualmente.
- El firebaseConfig ya está pegado (es el mismo proyecto que ya tenías).

PASOS:
1) En Firebase Console > Firestore Database > Rules, pega el contenido
   de firebase-rules.txt (reemplaza lo que había antes) y publica.
2) En Firebase Console > Authentication > Users > "Add user", crea una
   cuenta para ti (tu correo) y otra para Lisbeth, cada una con su
   propia contraseña. Esa es la única forma de entrar a la app.
3) Sube estos archivos (index.html, firebase-rules.txt, icon.svg,
   manifest.webmanifest, sw.js) a tu repositorio de GitHub, reemplazando
   los anteriores.
4) Publica con Firebase Hosting como ya lo hiciste antes.
5) Abre la URL HTTPS en Chrome del celular (tuyo y el de Lisbeth) y usa
   "Instalar aplicación" / "Agregar a pantalla de inicio". Cada uno
   inicia sesión con su propio correo y contraseña, pero ambos ven y
   registran en la misma lista de gastos, ingresos y ahorro.

SEGURIDAD:
- La seguridad real está en dos capas: (1) solo tú creas cuentas en
  Authentication, así que nadie más puede entrar; (2) las reglas de
  Firestore exigen "request.auth != null", es decir, solo alguien con
  sesión iniciada con una de esas cuentas puede leer o escribir datos.
- Si en algún momento quieres dar de baja el acceso de alguien, borra
  su usuario en Authentication > Users y pierde acceso de inmediato.
- Guarda bien las contraseñas; no hay recuperación automática salvo que
  actives "restablecer contraseña por correo" en Authentication.
