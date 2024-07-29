<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Age Clock</title>
    <script>
        function calculateAge(birthDate) {
            const now = new Date();
            const ageDate = new Date(now - birthDate);
            return Math.abs(ageDate.getUTCFullYear() - 1970);
        }

        function updateAge() {
            const birthDate = new Date('2005-02-08'); // Your birthdate
            const age = calculateAge(birthDate);
            document.getElementById('ageDisplay').textContent = age;
        }

        window.onload = function() {
            updateAge();
            setInterval(updateAge, 86400000); // Update every 24 hours (86400000 milliseconds)
        }
    </script>
</head>
<body>
    <h1>Your Age: <span id="ageDisplay"></span></h1>
</body>
</html>
