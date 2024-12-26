# Love-test-by-astroyogi-
<!DOCTYPE html>
<html>
<head>
    <title>Love Test</title>
</head>
<body>
    <h1>Love Test</h1>
    <p>Enter your name and the name of your crush:</p>
    <form id="loveForm">
        <label for="yourName">Your Name:</label><br>
        <input type="text" id="yourName" name="yourName" required><br><br>
        
        <label for="crushName">Crush's Name:</label><br>
        <input type="text" id="crushName" name="crushName" required><br><br>
        
        <button type="button" onclick="calculateLove()">Test Love</button>
    </form>
    
    <p id="result"></p>
</body>

<script>
function calculateLove() {
    const yourName = document.getElementById('yourName').value;
    const crushName = document.getElementById('crushName').value;
    
    if (yourName && crushName) {
        const loveScore = Math.floor(Math.random() * 100) + 1; // Random score between 1 and 100
        const result = `${yourName} and ${crushName}'s love score is: ${loveScore}%! ❤️`;
        
        document.getElementById('result').innerText = result;

        // Simulate sending the result back to the sender
        alert(`Result sent to sender: ${result}`);
    } else {
        alert('Please fill in both names!');
    }
}
</script>
</html>
