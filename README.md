// 1️⃣ Generar un usuario aleatorio
const randomUsername = `user${Math.floor(Math.random() * 100000)}`;
const password = "Testim@123"; // Puedes cambiar esta contraseña

// 2️⃣ Hacer clic en el botón "Sign up" para abrir la modal
await testim.click("#signin2");

// 3️⃣ Esperar a que la modal de registro sea visible
await testim.waitForElement("#signInModal", 5000);

// 4️⃣ Ingresar el usuario y la contraseña en los campos de texto
await testim.setValue("#sign-username", randomUsername);
await testim.setValue("#sign-password", password);

// 5️⃣ Hacer clic en el botón "Sign up"
await testim.click("button[onclick='register()']");

// 6️⃣ Mostrar el usuario generado en la consola
console.log("Usuario registrado:", randomUsername);
