<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>Wedding Invitation</title>

<link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@500&family=Poppins&display=swap" rel="stylesheet">

<style>
body {
  margin: 0;
  font-family: 'Poppins', sans-serif;
  background: #fdfaf6;
  color: #333;
  text-align: center;
}

/* HERO */
.hero {
  height: 100vh;
  background: url('https://images.unsplash.com/photo-1519741497674-611481863552') center/cover;
  display: flex;
  flex-direction: column;
  justify-content: center;
  color: white;
  animation: fadeIn 2s ease;
}

.hero h1 {
  font-family: 'Playfair Display', serif;
  font-size: 42px;
}

.hero p {
  font-size: 18px;
}

/* CARD */
.card {
  background: white;
  margin: -60px auto 20px;
  padding: 30px;
  max-width: 400px;
  border-radius: 16px;
  box-shadow: 0 8px 25px rgba(0,0,0,0.1);
  animation: slideUp 1.5s ease;
}

h2 {
  font-family: 'Playfair Display', serif;
}

/* RSVP */
.rsvp {
  padding: 40px 20px;
}

input {
  width: 80%;
  padding: 12px;
  margin: 10px 0;
  border-radius: 8px;
  border: 1px solid #ccc;
}

button {
  background: #c89b6d;
  color: white;
  border: none;
  padding: 12px 25px;
  border-radius: 8px;
  font-size: 16px;
  cursor: pointer;
}

/* ANIMATIONS */
@keyframes fadeIn {
  from {opacity: 0;}
  to {opacity: 1;}
}

@keyframes slideUp {
  from {transform: translateY(40px); opacity: 0;}
  to {transform: translateY(0); opacity: 1;}
}

</style>
</head>

<body>

<div class="hero">
  <h1>Hujji & Partner</h1>
  <p>We’re getting married 💍</p>
  <p>20 May 2026</p>
</div>

<div class="card">
  <h2>Wedding Details</h2>
  <p>📅 20 May 2026</p>
  <p>⏰ 6:00 PM</p>
  <p>📍 Grand Hall, Your City</p>
</div>

<div class="rsvp">
  <h2>RSVP</h2>

  <form onsubmit="submitRSVP(event)">
    <input type="text" placeholder="Your Name" required><br>
    <input type="number" placeholder="Number of Guests" required><br>
    <button type="submit">Confirm Attendance</button>
  </form>

  <p id="msg"></p>
</div>

<script>
function submitRSVP(e) {
  e.preventDefault();
  document.getElementById("msg").innerText = "✅ Thank you! RSVP received.";
}
</script>

</body>
</html>
